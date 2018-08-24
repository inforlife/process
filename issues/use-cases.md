---
layout: page
title:  "Use Cases"
---

We structure use cases as follows.

## Title
Few words that identify the functionality to be added. Whenever possible, prefer names that begin with a verb instead of a noun.

An example of a name is `Email the report on a monthly basis`.

## Primary actor
The main system involved in the completion of the use case.

An example of primary actor is `The application`.

## Preconditions
A description of the state the involved systems must be in at the begin of the use case.

An example of preconditions is `The application can communicate with the ERP System`.

## Minimal Guarantees
The minimum expected outcome when the main success scenario can't successfully complete.

An example of minimal guarantees is `An error message is logged out`.

## Success Guarantees
The expected outcome when the main success scenario is completed.

An example of success guarantees is `The report is emailed to the predefined email address(es)`.

## Trigger
The event that causes the use case to begin.

An example of a trigger is `It's Monday 6AM`.

## Main Success Scenario
A description of the flow of events from preconditions to postconditions, when nothing goes wrong.

An example of scenario is

{% highlight yaml %}
- The application retrieves batch information from the ERP System.
- The application filters the lists all batches.
- The application generates a PDF report including the batches expiring within the following seven days.
- The application emails the PDF report to the predefined email address(es).
{% endhighlight %}

## Conditions of satisfaction
A checklist that includes all the criteria the feature should meet in order to consider its implementation completed.

An example of a conditions of satisfaction is

{% highlight yaml %}
- A PDF report is generated every Monday at 6AM.
- The generated PDF report lists all the batches expiring within the following seven days.
- The generated PDF report is emailed to a predefined list of address(es).
{% endhighlight %}

**Features without conditions of satisfaction cannot be included in a Milestone.**

Conditions of satisfaction are usually checked as they are implemented.

If new conditions arise, they are added until the corresponding Pull Request is not merged.

## Pull request
Since we have decided to refer the Issue number in a comment when opening Pull requests, GitHub automatically links the Issue to the Pull request that implements it. This allows us to have full traceability.

## Labels
At least `Feature` is assigned to the issue.
Other labels may be assigned according to specific needs.

## Attachment *optional*
Artifacts related to the feature such as diagrams may be attached to the Issue.
