---
layout: page
title:  "Continuous Integration"
---

[Continuous Integration](http://martinfowler.com/articles/continuousIntegration.html) (CI) is a software development practice where members of a team integrate their code frequently against a controlled source code repository. This can ensure nothing specific to the developer's machine is making the tests pass or features developed in parallel may create side effects when merged together.

Thanks to the integrations offered by GitHub, every time new code is pushed to Github, [CircleCI](https://circleci.com/) (the CI service we currently use) generates an automated build, verifying the integration of the new code with the existing code base and posts the outcome directly on GitHub pull request.

GitHub now allows us to enforce a rule that a pull request may be merged **only** if all the checks (in our case just the CI build) pass. **This guarantees that it is not possible for code with failing specifications to move from a feature branch to development and eventually to production**.

One of the reason why we have chosen CircleCI is because it allows us to configure our build process through a [configuration file](https://circleci.com/docs/configuration/) that is part of the repository itself. In this way, it is very clear which actions are performed as part of the build and it is easy to update those actions when necessary.

In addition to the correctness of the spec suite, the build also checks for the correctness of the [Docker image](https://docs.docker.com/engine/userguide/containers/dockerimages/). This guarantees that possible errors in the image are found way before the official image is built and stored in [Docker Hub](https://hub.docker.com/).

An history of all the builds done throughout the project, may be found on CircleCI web application.
