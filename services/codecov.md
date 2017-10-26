---
layout: page
---

# [CodeCov](https://codecov.io/)

Codecov is a service that delivers coverage metrics directly into pull requests.

To have CodeCov posting code coverage data to GitHub after a CI built is completed, CodeCov has to be integrated with both GitHub and the CI service.

The integration with GitHub is automatically done by GitHub itself since CodeCov has access to all the `inforlife` repositories. This allows CodeCov to post data to the pull request pages in GitHub.

We refer to the [CodeShip documentation](https://documentation.codeship.com/general/integrations/codecov/) to integrate CodeShip with CodeCov.

<span class="alert warning">deprecated</span> For CircleCI, we add the `CODECOV_TOKEN` to the project via CircleCI UI.
