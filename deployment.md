---
layout: page
title:  "Deployment"
---

We have opted for [Docker](https://www.docker.com/) as infrastructural platform to run in production.

Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow us to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. By doing so, thanks to the container, we can rest assured that the application will run on any other machine regardless of any customized settings that machine might have that could differ from the machine used for writing and testing the code.

When the images has been published to the [InfoRLife's Registry](https://github.com/inforlife/registry) as [GitHub Package](https://github.com/features/packages), we deploy the release to production.

Despite our efforts, the steps required to deploy each application still vary from application to application (especially for the first deployment) so we document all of them in a [dedicated GitHub Repository](https://github.com/inforlife/operations)[2](#notes).

We are trying with each iteration to reduce those differences and we are aiming at reaching a point where all we have to do for a deployment is simply to upload to Rancher the `docker-compose.yml` and the `rancher-compose.yml` files and let Rancher do the rest.

As part of the booting process, all applications log their release version to [Papertrail](https://inforlife.github.io/process/services/papertrail.html). This allows all the team members and our QA unit to be notified when something is deployed to production.


#####Notes:
1. Legacy applications may have different protocols which need to be reviewed before each deployment.
2. Since the Operations Repository is currently private, you must have granted access to be able to see it.
