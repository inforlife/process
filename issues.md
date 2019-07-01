---
layout: page
title:  "Issues"
---

We manage project requirements (both functional and non-functional) with GitHub Issues. Thus, we refer to requirements as issues.

Keeping the issues directly on GitHub, it makes easy to link them to the branch (and pull request) that implements them and to ensure full [traceability](https://inforlife.github.io/process/traceability.html) in the source code. In this way, issues' history is available to anyone who would like to audit it.

Every collaborator of the project who wishes to add a new issue creates a new GitHub Issue where he describes what he would like to be implemented or the error he has found. Once done, the collaborator assigns the Issue to a development team member.

To ensure we have developed what needed, `features` and `fixes` have to be accepted before they can be considered `done` and ready for deployment. This means the person needing a feature or founding a bug needs to be clearly identified. Thus, we encourage all users to actively collaborate on the projects and open Issues by themselves.

The team member reviews (alone or with other members) the issue in order to gather any missing information and, if needed, to standardize it.

When that is not possible, we open Issues on their behalf. In this case, once drafted, the Issue is assigned to the original petitioner who confirms the correctness of the Issue by adding the `Endorsed` label. If the Issue is not correct, petitioner and a team member collaborate to clarify any incorrect point. Then, the Issue is endorsed.

The `support request` label is added to all the issues initiated by an end-user so, we can keep track of the amount of support needed by the users.

Once a team member acknowledges the existence of the new issue, he adds the `addressed` label. In this way, we can calculate the response time to each Issue.

As soon as a new defect is confirmed, the team member who verified it notifies all the users about it. When possible, a temporary workaround should be provided.  Then, he adds the `notified` label to the Issue. The label allows us to keep track of the time elapsed between the notification and release of the fix.

We have divided GitHub Issues into the five categories below.

- [Features](https://inforlife.github.io/process/issues/features.html)
- [Fixes](https://inforlife.github.io/process/issues/fixes.html)
- [Enhancements](https://inforlife.github.io/process/issues/enhancements.html)
- [Payoffs](https://inforlife.github.io/process/issues/payoffs.html)
- [Others](https://inforlife.github.io/process/issues/others.html)

According to its category, a GitHub Issue needs specific information to be considered complete and so ready to be implemented.

<div class="alert info">The only updates allowed without being described in an Issue are "dependency upgrades" such are upgrading the version of the Ruby programming language or that of a Ruby Gem used for the project.
Any other change in the source code must become from an approved/confirmed GitHub Issue.</div>

## Approval or Confirmation

Once the team member considers the issue ready for implementation, it assigns it to an issue approver. If multiple approvers are collaborating on a repository, the team member simply picks one up.

The approver then reviews the issue and approves (or rejects) its implementation by assigning to the Issue the corresponding Label. The approver may also add a comment.

We require an approval from QA only for `features` and `enhancements`.
`Payoffs` and `others` are approved by the development team.
`Fixes` are confirmed by a member of the development team.

# Nullification

Issues may need to be nullified at some stage of their life. That may happen due to changes in the requirements, because the same outcome can be achieved in a different way or for other reason.

When this happens, according to the stage the Issue is currently in, a different course of action is taken.

- If it hasn't been implemented yet, the Issue is simply closed and the  `Nullified` Label is attached to it.
- If it is under development, the Pull Request is closed, the issue branch is deleted then, the Issue is closed and the  `Nullified` Label is attached to it.
- If it has been already merged into `master` (Pull Request closed), a new Issue is created indicating the functionalities provided by the original Issue must be removed. This new issue follows the standard [development process](https://inforlife.github.io/process/development.html).
