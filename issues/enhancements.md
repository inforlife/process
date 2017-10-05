---
layout: page
title:  "Enhancements"
---

Enhancements are those issues that improve a functionality without adding new capabilities. These issues are usually user-interaction related.

We structure `enhancements` as follows.

## Title
Few words that identify the enhancement.

An example of name is `Minify the form when displaying the results`.

## Description
A summary of the current (interface) design downside. When possible, the description should link back to the card that originally implemented the feature.

An example of description is

The search form does not minify when results are displayed and, due to its size, it may be difficult to notice the results are displayed below it.
This enhances [display results].

## Conditions of satisfaction
A checklist that includes all the criteria the feature should meet in order to consider the enhancement completed.

An example of conditions of satisfaction is

{% highlight yaml %}
- When results are displayed the search form is minified.
- The minified form can be extended again.
{% endhighlight %}

**Enhancements without conditions of satisfaction cannot be included in a Milestone.**

Conditions of satisfaction are usually checked as they are implemented.

If new conditions arise, they are added until the corresponding Pull request is not merged.

## Pull request
Since we have decided to refer the Issue number in a comment when opening Pull requests, GitHub automatically links the Issue to the Pull request that implements it. This allows us to have full traceability.

## Labels
At least `Enhancement` is assigned to the issue.
Other labels may be assigned according to specific needs.

## Attachment *optional*
Artifacts related to the enhancement such as wireframes or screenshots may be attached to the Issue.
