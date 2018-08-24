---
layout: page
title:  "Payoffs"
---

Payoffs reduce [technical debt](http://martinfowler.com/bliki/TechnicalDebt.html). They make the design cleaner without introducing new functionalities.

## Name
Few words that identify the improvement.

An example of a name is `Optimize notifications`

## Description
A summary of the concerns with the current design.

When possible, the description should link back to the issue that originally introduced the debt.

An example of a description is

{% highlight yaml %}
The current design doesn't allow to easily introduce, in addition to email, other forms of communication such as push notification or SMS.

This pays off debt introduced in [reset password].
{% endhighlight %}

## Pull request
Since we have decided to refer the Issue number in a comment when opening Pull requests, GitHub automatically links the Issue to the Pull request that implements it. This allows us to have full traceability.

## Labels
At least `Payoff` should be assigned to the card.
Other labels may be assigned according to specific needs.
