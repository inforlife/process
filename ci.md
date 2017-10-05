---
layout: page
title:  "Continuous Integration"
---

[Continuous Integration](http://martinfowler.com/articles/continuousIntegration.html) (CI) is a software development practice where members of a team integrate their code frequently against a controlled source code repository. This can ensure nothing specific to the developer's machine is making the tests pass or features developed in parallel may create side effects when merged together.

Thanks to the features offered by GitHub, every time new code is pushed to Github, a CI service generates an automated build, verifying the integration of the new code with the existing code base and posts the outcome directly to GitHub Pull request.

Due to the standard protection rules, we define on each repository, any Pull request may be merged **only** if all CI build passes.

**This guarantees that it is not possible for code with failing specifications to move from a feature branch to master and eventually to production**.

All the CI services we use allow us to configure our build process through configuration files that are checked in as part of the repository itself. In this way, the configuration is reviewed like all the other code and it is easy to update those actions when necessary. Moreover, it is always clear which actions are performed during the build.

A history of all the builds done throughout the project may be found browsing the CI service web application.
