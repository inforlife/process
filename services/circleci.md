---
layout: page
---

# <span class="alert warning">deprecated</span> [CircleCI](https://circleci.com/)


CircleCI is a hosted continuous integration and delivery system.

To integrate the GitHub Repository with CircleCI, the following steps are executed.

- We add the `circle.yml` (<span class="alert warning">deprecated</span> for CircleCI 1.0) or `.circleci/config.yml`(for CircleCI 2.0) configuration file to the repository.
- In CircleCI, we add the project.

<div class="alert info">Make sure the repo includes the configuration file before connecting it to CircleCI since the service will build `master` right after the connection is established.</div>
