---
layout: page
---

# [Papertrail](https://papertrailapp.com/)

Papertrail is a cloud-hosted log management service that consolidates application logs in one single place.

We refer to the [Papertrail documentation](https://help.papertrailapp.com/kb/configuration/configuring-centralized-logging-from-ruby-on-rails-apps/#method-a-use-papertrails-tiny-remote_syslog2-daemon) to integrate Papertrail with our application.

We have set [alerts](https://help.papertrailapp.com/kb/how-it-works/alerts/) up so after each deployment, Papertrail notifies the development team via Slack and the QA unit via email.

Our current plan allows us to store up to 1 gigabyte per month. With 1-week search capability and 1-year archive.
