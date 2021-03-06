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
- All the Issues associated with the Milestone MILESTONE have the required Labels (`Approved`/`Confirmed` and `Accepted`).
- A Release having `tag version` equal to MILESTONE doesn't exist already.
- The last CI build for the `master` branch (the one which will be released) of the Repository REPOSITORY was successful.

If all the checks are successful, it drafts, from the `master` branch, the MILESTONE release and closes the Milestone MILESTONE. Otherwise, it posts back to the `devops` channel an informative message.

Once the release has been drafted, InfoRBot publishes the updated documentation (the content of the `\doc` directory) to the documentation site.

We then [archive](https://blog.github.com/2018-06-28-archive-project-board-cards/) all the done issues.

## Image build

When the new Release is drafted, the [Publish Docker Image To GitHub Packages](https://github.com/inforlife/publish-docker-image-to-github-packages-action) [Action](https://github.com/features/actions) runs and, according to the Dockerfile[1](#notes) it finds inside the repo, builds a Docker image tagged with the same `tag` assigned to the Release (i.e. 2018.1) and publishes it to the [InfoRLife's Registry](https://github.com/inforlife/registry) as [GitHub Package](https://github.com/features/packages).

Once the image is published, we receive a notification in a dedicated [Slack](https://inforlife.github.io/process/services/slack.html) channel and we are ready for [deployment](https://inforlife.github.io/process/services/deployment.html).

Even if the current process may be further improved with the adoption of automated deployment, we have reached a level of automation that allows us to create a new GitHub Release and to have that code ready for production in less than half hour without any human intervention.

This level of automation first and foremost guarantees that every release is done in a predictable way eliminating any possible error or omission due to humans. Therefore, the activities needed to qualify the drafting of a new release (not a deployment) have become superfluous and can be skipped.

## Non-production releases

From time to time it may be necessary to draft a non-production (beta) release. This may be necessary to test integration with other applications or to allow final users to verify if new features have been implemented as they intended. In this case, the release is drafted manually by a team member. Beta releases are tagged as YYYY.N.bX where YYYY is the year of the release, N is the release progressive number, and  X is the beta progressive number. For instance, 2018.1.b2 identifies the second beta of the first release drafted in 2018. In addition, the release is marked as a pre-release so, in GitHub, it is visible the release is non-production ready.   

#####Notes:
1. A Dockerfile is a file that contains all the instructions necessary to build the Docker Image, these instructions may be to pull a third-party software from a registry or to execute a specific command. For more information refer to the [Docker documentation](https://docs.docker.com/engine/reference/builder/).
