---
layout: page
title:  "Operations"
---

We have put so much effort in developing and deploying our applications to production that we try our best to keep them running.

## Uptime Monitoring

For the applications accessible through the Internet, we use [Updown](https://inforlife.github.io/process/services/updown.html) to periodically check their availability.

For the applications accessible only from within the InfoRLife LAN, we currently rely on users for downtime notifications. Since all applications are heavily used we have found that the easiest way to be notified if something isn't working properly.

We have also looked for a simple system that automates the monitoring of those applications without Internet access but, we haven't find the right one yet.

## Data Backup

The backup of all our applications data is automatically executed daily and stored on the corporate Barracuda Backup system.
