---
layout: page
title:  "Iterations"
---

Due to some peculiarities of our team, first of all, the fact that we can't be fully dedicated to software development, we agreed an iterative approach works better than traditional [waterfall](http://en.wikipedia.org/wiki/Waterfall_model) for us.

We break down the development of an application into smaller chunks (iterations). On each iteration, new [issues](https://inforlife.github.io/process/issues.html) are designed, developed and tested until they are considered 'done'.

We define an issue 'done' as an issue which has all its *conditions of satisfaction* implemented and it has been *accepted* by its owner.

At the end of each iteration, we release the issues completed during that cycle and deploy them to production.

We schedule new iterations according to our workload, the number of approved issues we have in the pipeline and their business criticality.  

We don't time-box iterations, the span of an iteration depends on the number of issues we have to complete. Said so, we try to keep iterations as short as possible. Ideally, an iteration doesn't last for more than two weeks.

## Milestones
While issues are gathered, reviewed, and approved as soon as they arise, they are prioritized only right before an iteration is scheduled to begin.

First, a new GitHub Milestone is created and all the approved issues which will be implemented during the iteration are associated with it.

Milestones are simply named as YYYY.X where YYYY is the year when the milestone is opened and X is a progressive number. For instance, 2017.1 is the first milestone for the year 2017.  It may happen a milestone is closed the year after it is opened. That is perfectly fine with us and we don't find the need to update its name.

Once the Milestone has been created, the team leader adds all issues planned to be implemented to the 'Backlog' column of the `Development` Project and prioritizes them placing the most relevant above all others. He may also assign specific Issues to specific team members.

At this point, the [development process](https://inforlife.github.io/process/development.html) can begin.

## User Acceptance
During an iteration, the development team periodically (usually on a weekly basis) demonstrates all the issues already completed and not considered 'done' yet.

At the demo participate all the owners of issues planned to be demonstrated (they are notified in advance by the development team).

Any other collaborator or user of the application is welcome to join the demo session.

After the demo, each issue owner accepts the issue or request further changes. To accept it, the owner simply adds the `Accepted` Label to the Issue. In case changes are required, the issue owner adds them as a comment to the Issue.

Accepted Issues are moved, by a member of the development team, to the 'Done' column in the `Development` Project and it is considered ready to be shipped. The Issue is also closed.

Issues that require changes are put back to the 'Backlog' column in the `Development` Project so the changes can be implemented following the standard [development process](https://inforlife.github.io/process/development.html).
