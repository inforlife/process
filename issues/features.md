---
layout: page
title:  "Features"
---

Features are those issues that introduce a new functionality to the application or modify (usually extend) an existing one.
We have decided to express them as modified slightly [user stories](https://www.mountaingoatsoftware.com/agile/user-stories), in this way they can be read as functional specifications.

We structure `features` as follows.

## Title
Few words that identify the functionality to be added. Whenever possible, prefer names that begin with a verb instead of a noun.

An example of name is `Reset password`.

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

**Features without conditions of satisfaction cannot be included in a Milestone.**

Conditions of satisfaction are usually checked as they are implemented.

If new conditions arise, they are added until the corresponding Pull request is not merged.

## Pull request
Since we have decided to refer the Issue number in a comment when opening Pull requests, GitHub automatically links the Issue to the Pull request that implements it. This allows us to have full traceability.

## Labels
At least `Feature` is assigned to the issue.
Other labels may be assigned according to specific needs.

## Attachment *optional*
Artifacts related to the feature such as wireframes or mockups may be attached to the Issue.


# Story Sizing

Like many other aspects of software product management, there isn’t a universal right size for a user story. A user story may require from a couple of hours to a few days to be implemented. When defining user stories, we apply the following criteria.

 - A story should be small enough for the team to understand it
 - A story should be small enough to be created in in a short time period
 - A story should be big enough to represent business value in its own right
 - A story should be big enough to be deliverable in its own right

In case a feature seems too big, it can be broken down into multiple stories.
