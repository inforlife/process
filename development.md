---
layout: page
title:  "Development"
---

When a team member is ready to start working on a new issue, he accesses the `Development` Project and looks, in the 'Backlog' column, for Issues assigned to him.

If he finds one, he moves it to the `In progress` column.

If no Issues are currently assigned to the team member, he picks up, from the 'Backlog' column, the one above all others (the currently most relevant), assigns it to him and, moves it to the `In progress` column.

At this point, the team member creates locally an 'issue' branch named after the issue title and implements one after the other all the *Conditions of satisfaction* listed in the Issue using [Test-Driven Development](https://inforlife.github.io/process/test-driven-development.html).

The new code is pushed regularly to GitHub (at least one per day).

After the first push, the team member opens in GitHub a [Pull request](https://help.github.com/articles/using-pull-requests) to merge the issue branch into `master`. By default, the comment field is pre-populated with `This PR refers to issue #`, the branch owner adds the number of the Issue, so we can trace the Issue within the code.

After every push to GitHub, the code goes through [CI](https://inforlife.github.io/process/ci.html)[1](#notes), to ensure all the tests pass, and through Code Climate which looks for and reports quality issues.

When the issue has been implemented in all its parts (all conditions of satisfaction are met), the code must be [reviewed](https://inforlife.github.io/process/code-review.html) before it can be merged into `master`. Thus, the branch owner, after making sure all the required checks pass, selects a reviewer (another member of the team).

The branch owner is allowed to require a code review when Code Climate fails because of "false-positives", those issues that the branch owner retains irrelevant. All relevant violations raised by Code Climate are addressed before starting the code review.

As soon as possible, the reviewer goes through the Pull Request.

Once the review is completed, branch owner and reviewer meet (physically or remotely) and complete the review by going together through any relevant comment.

If the code requires any change, the branch owner updates it. Once the reviewer approves the updated code, the branch owner can merge the branch into `master` and delete it.

If the reviewer did not require changes, the branch owner can merge the branch as soon as the review is completed.

At this point, the team member who implemented it, closes the Issue and moves the relative card to the 'Completed' column in the `Development` Project.

<div class="alert info">We believe that code review is the single biggest thing we can do to improve the quality of the code we produce and, as very positive side effect, it also improves team members' skills.</div>

#####Notes:
1. This does not apply to `legacy` application which aren't developed using TDD.
