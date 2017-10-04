---
layout: page
title:  "Project setup"
---

When a new project begins, a GitHub repository is created and all the necessary services configured.

# GitHub
A new repository, named after the project, is created. This may be done following the [Github documentation](https://help.github.com/articles/create-a-repo/) or forking the [alpha repository](https://github.com/inforlife/alpha) which include samples for all the required configuration files.

Due to the size of the development team and the fact personnel external to the team is still marginally involved, we use the `inforlife` GitHub personal account[1](#notes) as the organizational account. This allows us to keep things simple (and cheap).

All members of the development team and [inforbot](https://github.com/inforbot) are added as collaborators to the repository.

At least one issue owner [2](#notes)(a member of the QA unit) is added as a collaborator.

Other personnel is added upon their request. We welcome all the users as collaborators.

Several labels are added to the repository, among those are included the following

- Enhancement
- Feature
- Fix
- Payoff

The `master` branch is protected with the following policy

- Require pull request reviews before merging;
- Dismiss stale pull request approvals when new commits are pushed;
- Require status checks to pass before merging.
- Require branches to be up to date before merging
- Include administrators

This policy assures first of all the `master` branch can't be accidentally be deleted and code can't be directly added to it. In addition, any other branch must have a formal approval by a team member and have passed all the 'required' automatic checks before being mergeable into `master`.

The automatic checks currently in place are

- codeclimate [Required]
- codecov/project [Required]
- continuous-integration/codeship or ci/circleci [Required]
- codecov/patch
- codeclimate/coverage [CHECK NAME]

All the required checks are marked as such after the first post to an open Pull request.

# Continous Integration (CI)
The GitHub repository is connected to a CI service [3](#notes) in order to have the entire test suite automatically executed every time new code is pushed to GitHub.

Each application is connected to one of the CI services below based on the type of application.

## [CodeShip Pro](http://codeship.com/features/pro)

- A Dockerfile is added to the repo.
- The [services configuration file](https://documentation.codeship.com/pro/builds-and-configuration/services/) is added to the repo.
- The [steps configuration file](https://documentation.codeship.com/pro/builds-and-configuration/steps/) is added to the repo.
- The project is added in CodeShip.

## [CircleCI](https://circleci.com/) *deprecated*

- The configuration file, `circle.yml` (for CircleCI 1.0  *deprecated*) or `.circleci/config.yml`(for CircleCI 2.0) is added to the repo.
- The project is added in CircleCI.

**Make sure the repo includes the configuration file before connecting it to CircleCI since the service will build `master` right after the connection is established.**

# [Code Climate](https://codeclimate.com)
The GitHub repository is connected to Code Climate for quality metrics and code coverage.

## Quality Metrics
Similar to CI, after pushing code to GitHub, Code Climate runs the code against several static analysis tools (the tool list can be configured via the `.codeclimate.yml` file) to find code-related issues such as style inconsistency, duplication or complexity.

	-  The `.codeclimate.yml` file is added to the repo.
	-  The project is added in Code Climate.
	- The PR integration is configured.

TO ADD HOW TO DO CODE REVIEW ON CODE CLIMATE

## Code Coverage *experimental*
TO BE ADDED

This may, at some point in the future, replace CodeCov.

# [CodeCov](https://codecov.io/)
To assure the automatic test suite that comes with any application fully test the application is all its parts, we run [code coverage](https://en.wikipedia.org/wiki/Code_coverage) on each Pull request.

The GitHub repository and CI service are connected to CodeCov in order to get code coverage after each push to GitHub.

CodeCov receives from the CI service the report generated while running the entire test suite and posts the results to the GitHub Pull request.

While aiming at 100% code coverage is, in theory, a good thing, in the real world is impracticable or requires more effort than providing benefits. Thus, we have decided to define as acceptable threshold 90% code coverage for all our applications. When this threshold is not reached, `codecov/project` fails and Pull requests can't be merged into `master` until that value is reached again.

TO ADD INTEGRATION STEPS FOR CODESHIP
TO ADD INTEGRATION STEPS FOR CIRCLECI


# [Snyk](https://snyk.io/) *experimental*
The GitHub repository is connected to Snyk in order to find vulnerabilities in our code and its dependencies.

TO ADD INTEGRATION STEPS

# [Docker Hub](https://docs.docker.com/docker-hub/)
The GitHub repository is connected to Docker Hub, a registry service that builds and stores Docker images providing a centralized resource for image distribution and change management.

Each GitHub repository is connected to Docker Hub through an `Automated build` using the following build settings.

| Type 	| Name 	| Dockerfile Location 	| Docker Tag Name 	|
|------	|------	|---------------------	|-----------------	|
| Tag  	| /.*/ 	| /                   	| latest          	|
| Tag  	| /.*/ 	| /                   	| Same as tag     	|

This allows us to automatically trigger the build of two new images on Docker Hub upon drafting a new GitHub Release. The images are tagged one as `latest` (and used for deployment) and the other as the Release (for reference).

The integration may be configured following the [Docker documentation](https://docs.docker.com/docker-hub/builds/).


#####Notes:

1. The `inforlife` account is managed by the Development Team Leader.
2. For more details regarding issue owners may be found at the [issue gathering page](https://inforlife.github.io/process/issue-gathering.html).
3. For more details regarding Continous Integration may be found at the [CI page](https://inforlife.github.io/process/ci.html)
