---
layout: page
title:  "Fixes"
---

Fixes solve an error, flaw, failure or fault in an application that causes it to produce an incorrect or unexpected behavior.

We structure `fixes` as follows.

## Name
Few words that identify the correct or expected behavior. Name should include the verb *must*.

An example of a name is `Reset password must send only one email to account holder`.

## Description
All available information regarding the problem.

When possible, the description should link back to the GitHub Issue that originally implemented the feature.

An example of a description is

{% highlight yaml %}
When system administrator initiates a password reset, instead of receiving a single message, the account holder receives one email on each loaded locale.

This fixes a misbehavior introduced in [reset password].
{% endhighlight %}

## Conditions of satisfaction
A checklist that includes all the criteria that must be true to consider the problem solved.

An example of a conditions of satisfaction is

{% highlight yaml %}
- Only one message is sent to email address associated with the account.
- The message is localized according to account holder profile.
{% endhighlight %}

**Fixes without conditions of satisfaction cannot be included in a Milestone.**

Conditions of satisfaction have to be checked as they are implemented.

If new conditions arise, they are added until the corresponding Pull request is not merged.

## Pull request
Since we have decided to refer the Issue number in a comment when opening Pull requests, GitHub automatically links the Issue to the Pull request that implements it. This allows us to have full traceability.

## Labels
At least `Fix` should be assigned to the card.
Other labels may be assigned according to specific needs.

## Attachment *optional*
Artifacts related to the problem may be attached to the Issue. Screenshots are especially important when the issue is related to the user interface.
