---
layout: page
title:  "Code Review"
---

Once a [code review](https://help.github.com/articles/about-pull-request-reviews/) is assigned to a team member, the reviewer accesses the Pull request on GitHub and starts the review going through the code.
Whenever something doesn't seem fine and it may be improved, the reviewer adds a comment so it can be discussed with the branch owner later on.

Once completed, the reviewer assigns a status to the review. The possible statuses are

- Comment: Submit general feedback without explicitly approving the changes or requesting additional changes.
- Approve: Submit feedback and approve merging the changes proposed in the Pull request.
- Request changes: Submit feedback that must be addressed before the Pull request can be merged.

It is highly recommended (but not required) to add a Review summary before submitting the review.

If during the review, the reviewer decides to make any changes to the code, instead of giving a status to the review, he assigns back the review to the branch owner for approval.

**Code review may be skipped for issues developed through [pair programming](https://en.wikipedia.org/wiki/Pair_programming).**

## Code Climate
If Code Climate finds some violations on the code added by the pull request, it returns a `fail` check and the Pull request cannot be merged.

As part of the code review, the reviewer goes through all the `New` issues on Code Climate and assigns them one of the possible statuses

- Confirmed: This is a legitimate issue that should be addressed.
- Invalid: This issue is a false-positive.
- Wontfix: The issue is legitimate, but it does not need to be addressed at this time.

While assigning a status, the reviewer may leave a comment. A comment is highly recommended for `Confirmed` and `Wontfix` statuses.

Confirmed issues are discussed with the branch owner after the review is completed.

Once there are no more `Confirmed` issues, the reviewer approves the review and, optionally, add a comment.

We do Code Climate reviews only when issues are raised. Thus, an approval is not expected if no issues are raised.

As of October 2017, Code Climate does not require a formal approval to post a passing check. If all issues have a state other than `New` or `Confirmed`, the check passes. We try our best to approve all the reviews in Code Climate even if not technically required.
