---
layout: page
---

# [GitHub](https://github.com/)

The new GitHub Repository may be created following the [Github documentation](https://help.github.com/articles/create-a-repo/) or forking the [alpha repository](https://github.com/inforlife/alpha) which include samples for all the configuration files we need.

## Collaborators

The collaborators added to each repository are

- All members of the development team
- [InfoRBot](https://github.com/inforbot).
- At least one issue owner [1](#notes)(a member of the QA unit)

Other personnel is added upon their request. We welcome all the users as collaborators.

## Labels

The labels below are added to the repository

- Enhancement
- Feature
- Fix
- Payoff

Other labels may be added according to the needs.

## Projects

The `Development` project is created to the repository. The project has the column below

- Backlog
- In Progress
- Completed
- Done

It is used to keep track of issue implementation and approval.

## Branch Protection

When protecting the `master` branch we activate the options below

- Require pull request reviews before merging
- Dismiss stale pull request approvals when new commits are pushed
- Require status checks to pass before merging
- Require branches to be up to date before merging
- Include administrators

Status checks are automatically sent, along side additional data, by the integrated services once they finish running. Their values can be either `pass` or `failure` and they can be `required` or `optional`.

The status checks currently in place are

- codeclimate (code quality) [Required]
- codecov/project [Required]
- continuous-integration/codeship or ci/circleci [Required]
- codecov/patch
- codeclimate/coverage [CHECK NAME]

With our setup, checks marked as `required` must `pass` in order to be able to merge an issue branch into `master`.


#####Notes:

1. For more details regarding issue owners may be found at the [issue gathering page](https://inforlife.github.io/process/issue-gathering.html).
