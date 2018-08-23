---
layout: page
title:  "Release"
---

Once all the Issues associated with a Milestone have been closed, a new [GitHub Release](https://help.github.com/articles/about-releases/) can be drafted. Releases are the mechanism we use for packing our applications for deployment.

The release process has been fully automated with the use of [InfoRBot](https://github.com/inforlife/inforbot), an application we have internally developed.

InfoRBot is a chatbot hosted on [Heroku](https://www.heroku.com/) and added to the `devops` channel of our [Slack](https://inforlife.github.io/process/services/slack.html) workspace. It is currently used only for drafting new Releases but we hope to extend its capabilities in the future.

To draft a new release, a team member posts a message to the `devops` channel of our Slack workspace with the following structure

`inforbot release REPOSITORY milestone MILESTONE`

Upon posting this message, InfoRBot runs the following checks

- The Repository REPOSITORY exists.
- The Milestone MILESTONE exists.
- All the Issues associated with the Milestone MILESTONE have been closed.
- A Release having `tag version` equal to MILESTONE doesn't exist already.
- The last CI build for the `master` branch (the one which will be released) of the Repository REPOSITORY was successful.

If all the checks are successful, it drafts, from the `master` branch, the MILESTONE release and closes the Milestone MILESTONE. Otherwise, it posts back to the `devops` channel an informative message.

Once the release has been drafted, InfoRBot publishes the updated documentation (the content of the `\doc` directory) to the documentation site.

## Image build

As soon as the new Release is drafted, [Docker Hub](https://inforlife.github.io/process/services/dockerhub.html) pulls the Release from GitHub and, according to the Dockerfile[1](#notes) it finds inside, builds and stores the two identical images we have configured it to create.

Once the images have been built, we are ready for [deployment](https://inforlife.github.io/process/services/deployment.html).

Even if the current process may be further improved with the adoption of automated deployment, we have reached a level of automation that allows us to create a new GitHub Release and to have that code ready for production in less than half hour without any human intervention.

This level of automation first and foremost guarantees that every release is done in a predictable way eliminating any possible error or omission due to humans. Therefore, the activities needed to qualify the drafting of a new release (not a deployment) have become superfluous and can be skipped.


#####Notes:
1. A Dockerfile is a file that contains all the instructions necessary to build the Docker Image, these instructions may be to pull a third-party software from a registry or to execute a specific command. For more information refer to the [Docker documentation](https://docs.docker.com/engine/reference/builder/).
