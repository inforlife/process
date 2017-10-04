---
layout: page
---

# [CircleCI](https://circleci.com/) *deprecated*

To integrate the GitHub Repository with CircleCI, the following steps are executed.

- We add the `circle.yml` (for CircleCI 1.0  *deprecated*) or `.circleci/config.yml`(for CircleCI 2.0) configuration file to the repository.
- In CircleCI, we add the project.

**Make sure the repo includes the configuration file before connecting it to CircleCI since the service will build `master` right after the connection is established.**
