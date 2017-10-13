---
layout: page
title:  "Test-Driven Development"
---

We use Test-Driven Development as development methodology. TDD is, according to [TestDrivenDevelopment by Martin Fowler](https://martinfowler.com/bliki/TestDrivenDevelopment.html),

> Test-Driven Development is a technique for building software that guides software development by writing tests. [...] In essence, you follow three simple steps repeatedly:
 Write a test for the next bit of functionality you want to add.
 Write the functional code until the test passes.
 Refactor both new and old code to make it well structured. You continue cycling through these three steps, one test at a time, building up the functionality of the system.

We write our tests as specifications using [RSpec](http://rspec.info/), a tool which allows us to automatically run the test suite through a command line interface.

## Specifications

We usually write two types of specifications, feature and class specifications.

### Feature Specifications

Feature specifications are end-to-end specifications written from the user perspective which, when executed, exercise the entire application stack. This type of specifications is written only for application with a user interface. For applications which don't require user interaction, we write a different kind of end-to-end specifications.

An example of feature specification is

{% highlight ruby %}
RSpec.feature "Log into the application", type: :feature do
  context 'when a user tries to log into the application' do
    context 'providing a valid password' do
      scenario 'he is redirected to the homepage' do
        visit root_path
        fill_in 'email',        with: user.email
        fill_in 'password',     with: user.password
        submit_form
        expect(page).to have_current_path(home_path)
      end
    end
  end
end
{% endhighlight %}

Without going into too many details[1](#notes), the specification describes how the application is supposed to work (when a user tries to log into the application providing a valid password he is redirected to the homepage) and verifies it by simulating the user interaction (filling out forms, clicking buttons and so on) and then asserting on the application state.  

We normally write a single specification (with multiple scenarios) for each [issue](https://inforlife.github.io/process/issues.html) we develop. Each scenario confirms a specific condition of satisfaction associated with the Issue.

### Class Specifications

Class specifications (also called unit tests) are lower-level specifications which individually and independently verify the correctness of a single class.

An example of class specification is

{% highlight ruby %}
RSpec.describe User, type: :model do
  let(:user_without_full_name) { build(:user, full_name: nil) }

  context "is not valid" do
    it "without a full name" do
      expect(user_without_full_name).to have_presence_validation_error_on(:full_name)
    end
  end
end
{% highlight %}

The specification describes the invalidity of, and therefore the impossibility to save into the database, a user without a full name.

Class specifications are focused on a single class and instances of that class thus they are executed in isolation. This means when interaction with other classes or objects is required, those interactions are often mocked[2](#notes).

We normally write a single specification (with multiple examples) for almost each class we have in our applications[3](#notes). Each example verifies a specific method defined within the class.


#####Notes:
1. For more details regarding RSpec syntax refer to [the documentation](https://relishapp.com/rspec/rspec-expectations/docs/syntax-configuration).
2. Mock objects are simulated objects that mimic the behavior of real objects in controlled ways
3. For a typical [Rails](http://rubyonrails.org/) application, we skip specifications only for controllers which are indirectly tested with feature specifications, and validators which are tested within the model they validate.
