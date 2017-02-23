---
layout: page
title:  "Project setup"
---

When an new project begins, the following tasks have to be executed in order to be able to use all the tools involved in the project management.

# GitHub

- A new repository has to be created. This may be done following the [Github documentation](https://help.github.com/articles/create-a-repo/). As starting point the [alpha](https://github.com/acsinfo/alpha) repostory may be used. 
- All members of the development team have to be added as collaborators (additional personnel may be also added).
- The following labels have to be created.
	- Feature
	- Fix
	- Payoff
    - Ready for review
    - Done

# CircleCI
The GitHub repository has to be added to CircleCI in order to have automatic specifications execution upon branch push to GitHub.

**Make sure the repo includes `circle.yml` before adding it to CircleCI.**


# Docker Hub

Before an application may be deployed to production for the first time An *Automated build* linked to the GitHub repo has to be created on Docker Hub. This may be done following the [Docker documentation](https://docs.docker.com/docker-hub/builds/). Refer to the `Image build` page in the project wiki for the project specific build settings.

This must be done before drafting the first release on GitHub.

# Docker Cloud

Before an application may run on production for the first time a new *Service* has to be created and deployed on Docker Cloud. This may be done following the [Docker documentation](https://docs.docker.com/docker-cloud/getting-started/your_first_service/). Refer to the `Service config` page in the project wiki for the project specific service configuration.
