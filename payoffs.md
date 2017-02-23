---
layout: page
title:  "Payoffs"
---

Payoffs reduce [technical debt](http://martinfowler.com/bliki/TechnicalDebt.html). They make the design cleaner without introducing new functionalities.

## Name
Few words that identify the improvement.

An example of name is `optimize notifications`

## Description
A summary of the concerns with the current design.

When possible, the description should link back to the issue that originally introduced the debt.

An example of description is

{% highlight yaml %}
The current design doesn't allow to easily introduce, in addition to email, other forms of communication such as push notification or SMS.

This pays off debt introduced in [reset password].
{% endhighlight %}

## PR
The link to the GitHub PR of the branch that reduces the technical debt. This is automatically added when the PR is opened by adding a reference to the issue itself.

## Labels
At least `Payoff` should be assigned to the card.

Other labels may be assigned according to specific needs.