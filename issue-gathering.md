---
layout: page
title:  "Issue Gathering"
---

We manage project requirements (both functional and non-functional) with GitHub Issues. Thus, we refer to requirements as issues.

Keeping the issues directly on GitHub, it makes easy to link them to the branch (and pull request) that implements them and to ensure full [traceability](https://inforlife.github.io/process/traceability.html) in the source code. In this way, issues' history is available to anyone who would like to audit it.

Every collaborator of the project who wishes to add a new issue creates a new GitHub Issue where he describes what he would like to be implemented or the error he has found. Once done, the collaborator assigns the Issue to a development team member.

The team member reviews (alone or with other members) the issue in order to gather any missing information and, if needed, to standardize it.

We have divided GitHub Issues into the five categories below.

- [Features](https://inforlife.github.io/process/issues/features.html)
- [Fixes](https://inforlife.github.io/process/issues/fixes.html)
- [Enhancements](https://inforlife.github.io/process/issues/enhancements.html)
- [Payoffs](https://inforlife.github.io/process/issues/payoffs.html)
- [Others](https://inforlife.github.io/process/issues/others.html)

According to its category, a GitHub Issue needs specific information to be considered complete and so ready to be implemented.

**The only updates allowed without being described in an Issue are "dependency upgrades" such are upgrading the version of the Ruby programming language or that of a Ruby Gem used for the project.
Any other change in the source code must become from an approved GitHub Issue.**

## Approval

Once the team member considers the issue ready for implementation, it assigns it to an issue approver. If multiple approvers are collaborating on a repository, the team member simply picks one up.

The approver then reviews the issue and approves (or rejects) its implementation by assigning to the Issue itself the corresponding Label. The approver may also add a comment.

Before the begin of an iteration, the team leader adds all the approved issues to the 'Backlog' column of the `Development` Project and prioritizes them placing the most relevant above all others. The team leader may also already assign specific Issues to specific team members.
