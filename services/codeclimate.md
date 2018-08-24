---
layout: page
---

# [Code Climate](https://codeclimate.com)

Code Climate is a service that incorporates fully-configurable test coverage and maintainability data throughout the development workflow, making quality improvement explicit, continuous, and ubiquitous.

We use Code Climate for quality metrics and code coverage.

## Quality Metrics

To setup quality metrics (static analysis), the following steps are executed.

  - We add the `.codeclimate.yml` file to the repository. This file defines  the tools used for the analysis.
  - In Code Climate, we add the project.
	- In Code Climate, the [GitHub Pull Requests](https://docs.codeclimate.com/v1.0/docs/github) integration is configured.

## [Code Coverage](https://docs.codeclimate.com/docs/configuring-test-coverage)

To setup code coverage, the following steps are executed.

  - We add the `simplecov`gem to the `test` and `ci` group.
  - We require `simplecov` for the `ci` environment. We keep the gem in the `test` group so we can run code coverage locally if needed.
  - We load the `reporter ID` (CC_TEST_REPORTER_ID) via environment variables to the CI environment.
  - We install the Code Climate reporter to the Docker image we use to run our CI.
  - We add Code Climate commands before and after running the specification suite.
