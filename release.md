---
layout: page
title:  "Release"
---

In the recent past, a lot of effort has been put into automating everything that must happen between taking the source code of a piece of software from GitHub and making the software running in production.

Even if the current process may be further automated with the adoption of [continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery) techniques, thanks to the integration between GitHub and [Docker Cloud](https://www.docker.com/products/docker-cloud), we have reached a level of automation that allows us to create a [new release on GitHub](https://help.github.com/articles/about-releases/) and to have that code running on production in less than half hour without any human intervention.

**This level of automation first and foremost guarantees that every deployment is done in a predictable way eliminating any possible error or omission due to humans and the activities needed to qualify a new release can be reduced to few simple checks.**

As a side effect, since qualification takes now very little time, we can deploy more often providing valuable software to users more quickly.

## Steps

Once a feature (or a set of features) is 'done', it is time to deploy it to production.

- A team member (usually the one that have closed the last pull request) drafts a new release on GitHub defining
  - Tag version[1](#notes). - an up to three number code that identifies the release.
  - Release title - a brief description of the release.
  - Release description - this must include the type of release (upgrade or update) and the change log.

- As soon as the new release is created the request to build a new Docker image is automatically sent to [Docker Hub](https://www.docker.com/products/docker-hub), the part of Docker Cloud responsible for managing Docker images.

- Docker Hub, once received the request, pulls the release from GitHub and, according to the Dockerfile[2](#notes), builds and stores the two identical images[3](#notes) with different tags.
  - One with the same tag of the release in GitHub for future reference.
  - One with *latest* as tag for automatic deployment.

- As soon as the new *latest* image is created Docker Cloud picks it up and automatically
  - Pushes it to production.
  - Stops the now outdated running container.
  - Starts an identical one using the newly created image.

As part of the booting process, all applications log the number of the release that is running to [Papertrail](https://papertrailapp.com/), the log management service we currently use.

The successful completion of a new release is notified to the development team with a message posted to the `papertrail` channel in [Slack](https://slack.com/), the service we are currently using to receive all feedback related to the internally developed applications.

#### First deployment

Before an application may be deployed to production for the first time, few steps are required. They are described in the [project setup](http://inforlife.github.io/process/setup.html) page.


#####Notes:
1. Tags are created using [semantic versioning](http://semver.org/).
2. A Dockerfile is a file that contains all the instructions necessary to build the Docker Image, these instructions may be to pull a third-party software from a registry or to execute a specific command. For more information refer to the [Docker documentation](https://docs.docker.com/engine/reference/builder/).
3. A Docker image is an inert, immutable file that can be executed as it was a physical computer.
