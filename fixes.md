---
layout: page
title:  "Fixes"
---

Fixes solve an error, flaw, failure or fault in the application that causes it to produce an incorrect or unexpected behavior.

## Name
Few words that identify the correct or expected behavior. Name should include the verb *must*.

An example of name is `reset password must send only one email to account holder`.

## Description
All available information regarding the problem.

When possible, the description should link back to the GitHub issue that originally implemented the feature.

An example of description is

{% highlight yaml %}
When system administrator initiates a password reset, instead of receiving a single message, the account holder receives one email on each locale.

This fixes a misbehavior introduced in [reset password].
{% endhighlight %}

## Conditions of satisfaction
A checklist that includes all the criteria that must be true to consider the problem solved.

An example of conditions of satisfaction is

{% highlight yaml %}
- Only one message is sent to email address associated with the account.
- The message is localized according to account holder profile.
{% endhighlight %}

**Fixes without conditions of satisfaction cannot move into implementation.**

Conditions of satisfaction have to be checked as they are implemented.

If new conditions arise, they may be added until the corresponding PR is not merged.
Fixes can be assigned to a reviewer only when all the conditions of satisfaction are checked out.


## PR
The link to the GitHub PR of the branch that fixes the problem. This is automatically added when the PR is opened by adding a reference to the issue itself.


## Labels
At least `Fix` should be assigned to the card.

Other labels may be assigned according to specific needs.


## Attachment

Artifacts related to the issue may be attached to the card. Screenshots are especially important when the issue is related to views.
