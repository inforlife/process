---
layout: page
title:  "Setup"
---

When a new project begins, a new [GitHub](https://inforlife.github.io/process/services/github.html) Repository, named after the project, is created.

Due to the size of the development team and the fact personnel external to the team is still marginally involved, we use the `inforlife` GitHub personal account[1](#notes) as the organizational account. This allows us to keep things simple (and cheap).
Because of that, once the repository has been created we add to it all the involved personnel as collaborators.

We add several labels and protection rules to the repository.

The `master` branch is protected with a policy which assures first of all it cannot be accidentally deleted and code can't be directly added to it. In addition, any other branch must have a formal approval by a team member and have passed all the 'required' automatic checks before being mergeable into `master`.

All the required checks are marked as such after the first post to an open Pull request which runs the check.

The GitHub Repository is connected to a CI service [2](#notes) in order to have the entire test suite automatically executed every time new code is pushed to GitHub.

Each application is connected either to [CodeShip](https://inforlife.github.io/process/services/codeship.html) or to [CircleCI](https://inforlife.github.io/process/services/circleci.html) based on the type of application.

The GitHub Repository is connected to [Code Climate](https://inforlife.github.io/process/services/codeclimate.html). Similar to CI, after pushing code to GitHub, Code Climate runs the code against several static analysis tools to find code-related issues such as style inconsistency, duplication or complexity. It also verifies [code coverage](https://en.wikipedia.org/wiki/Code_coverage) to assure the automatic test suite that comes with any application fully tests it in all its parts the code.

Code Climate receives from the CI service the report generated while running the entire test suite and posts the results to the GitHub Pull request.

While aiming at 100% code coverage is, in theory, a good thing, in the real world is impracticable or requires more effort than providing benefits. Thus, we have enforced Diff Coverage [3](#notes) with a 90% threshold and Total Coverage. In this way we check both the test coverage of the new code in each pull request (Diff Coverage) and how each pull request impacts overall test coverage of the repository (Total Coverage). When Diff Coverage is under 90% and Total Coverage decreases the relative check fails and Pull requests can't be merged into `master` until that overall coverage increases again.

Finally, the GitHub Repository is connected to [Snyk](https://inforlife.github.io/process/services/snyk.html) in order to find vulnerabilities in our code and its dependencies.

## Documentation site
We have found the best way to manage the documentation for the final users (the user manual) it is by handling it as source code and checking it into the project repository. This doesn't just allow us to be sure the documentation is updated alongside the application itself, reducing the risk of having outdated documentation, but it also let us automate its publishing with the [use of InfoRBot](https://inforlife.github.io/process/release.html).

To do so, alongside the creation of the project repository, we create a second repository for publishing the documentation named doc-PROJECT-NAME. We set to build a [GitHub Pages site](https://pages.github.com/) from the master branch and add InfoRBot as the only collaborator to the doc repository.


#####Notes:
1. The `inforlife` account is managed by the Development Team Leader.
2. For more details regarding Continuous Integration may be found at the [CI page](https://inforlife.github.io/process/ci.html)
3. The Diff Coverage threshold can currently defined only via the Code Climate UI. We will add it to source control as soon as it will be possible to define it in a configuration file.
