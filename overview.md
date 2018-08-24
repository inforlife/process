---
layout: page
title:  "Overview"
---

All our source code is managed using Git, a distributed version control system that keeps track of all the changes made during its life and shared using GitHub.

When we start working on a new project, we [setup](https://inforlife.github.io/process/setup.html) the GitHub repository and all the integrations (CI, static analysis, code coverage...) we need.

Besides providing a central repository where code can be synchronized, GitHub, thanks to the available integrations, has allowed us to build the entire life cycle around a single service providing all the pieces of evidence required by regulation while keeping the process fairly easy to understand.

We define the functionalities provided by our applications on GitHub Issues and [manage](https://inforlife.github.io/process/issues.html) them with GitHub Projects.

By keeping the functionalities directly in GitHub, we can easily link them to the branch where they are implemented and ensure full [traceability](https://inforlife.github.io/process/traceability.html) of any change in the source code. In this way, the entire application's history is available to anyone who would like to audit it.

We [develop](https://inforlife.github.io/process/development.html) in iterations. When a set of Issues is ready to be implemented, a GitHub Milestone is created, the Issues linked to it and prioritized.

Team members start implementing the issues according to their priority (from highest to lowest).

When a member starts working on a new issue, he opens a GitHub Pull request to merge the branch into `master`. This is helpful as everyone can see what the other members are working on by simply checking all the open Pull requests.

When completed, the issue [must be reviewed](https://inforlife.github.io/process/code-review.html) before it can be merged into `master`. So, after all automatic checks pass, the Pull request is assigned to a reviewer (another member of the team).

The reviewer looks through the Pull request and, according to the outcome of the review, approves it or requests changes.

Once the Pull Request is approved, the branch owner closes it by merging the branch into `master`. Then, she closes the Issue and moves the relative card to the 'Completed' column in the `Development` Project.

Periodically, completed Issues are shown to their owners in demo sessions at the end of which, they [accept them or ask for modifications](https://inforlife.github.io/process/iterations.html#user-acceptance).

Once an Issue is accepted, a team member moves the relative card to the 'Done' column in the `Development` Project.

When all the issues included in the milestone have been closed, we [release](https://inforlife.github.io/process/release.html) them via a GitHub Release and the code is deployed into production using Docker as the underlying platform.

We [operate](https://inforlife.github.io/process/operations.html) production applications to guarantee their availability and to maintain their validated state until their retirement.
