---
layout: page
title:  "Features"
---

Features introduce a new functionality to the application or modify (usually extend) an existing one.

## Title
Few words that identify the functionality to be added. Whenever possible, prefer names that begin with a verb instead of a noun.

An example of name is `reset password`.

## Description
A short and simple narrative of the feature told from the perspective of the person who will benefit from the new capability (usually a user of the application) that follows the template:

{% highlight yaml %}
[type of users] can
[some capability] so
[some reason].
{% endhighlight %}

An example of description is

{% highlight yaml %}
System administrators can
initiate account password resets so
forgetful users can access the application.
{% endhighlight %}

## Conditions of satisfaction
A checklist that includes all the criteria the feature should meet in order to consider its implementation completed.

An example of conditions of satisfaction is

{% highlight yaml %}
- Reset token is created.
- Reset token is sent to email address associated with the account.
- Reset token expires after a configurable period of time.
{% endhighlight %}

**Features without conditions of satisfaction cannot be included in a milestone.**

Conditions of satisfaction have to be checked as they are implemented.

If new conditions arise, they may be added until the corresponding PR is not merged.
Features can be assigned to a reviewer only when all the conditions of satisfaction are checked out.

## PR
The link to the GitHub PR of the branch that implements the feature. This is automatically added when the PR is opened by adding a reference to the issue itself.


## Labels
At least `Feature` should be assigned to the issue.

Other labels may be assigned according to specific needs.


## Attachment

Artifacts related to the feature such as wireframes or mockups may be attached to the card.
