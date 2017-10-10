---
layout: page
---

# [Slack](https://slack.com/)

Without going into too many details [what Slack is](https://get.slack.help/hc/en-us/articles/115004071768-What-is-Slack), we use it as "notification center" for all [DevOps](https://en.wikipedia.org/wiki/DevOps) related activities.

This allows us to receive, in a single place, all the feedback we need to be always informed about the state of our development and deployment.

We have created a dedicated Slack channel for each service we use. We currently have the following channels

- circleci, where the outcome of builts on CircleCI are posted.
- codeship, where the outcome of builts on CodeShip are posted.
- devops, where conversations with InforBot take place.
- docker-cloud *deprecated*, where the state of connection between Docker Cloud and the Dockyard node is updated.
- heroku, where the outcome of the deployment to [Heroku](https://www.heroku.com/) is updated.
- papertrail, where the confirmations of application deployment are posted.
- rollbar, where the errors raised by applications is production are posted.

All the messages are automatically posted by the respective services once a specific event happens.
