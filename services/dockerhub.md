---
layout: page
---

# [Docker Hub](https://docs.docker.com/docker-hub/)

Docker Hub is a registry service that builds and stores Docker images providing a centralized resource for image distribution and change management.

We refer to the [Docker documentation](https://docs.docker.com/docker-hub/builds/) to integrate GitHub with Docker Hub.

Each GitHub repository is connected to Docker Hub through an `Automated build` using the following build settings.

| Type 	| Name 	| Dockerfile Location 	| Docker Tag Name 	|
|------	|------	|---------------------	|-----------------	|
| Tag  	| /.*/ 	| /                   	| latest          	|
| Tag  	| /.*/ 	| /                   	| Same as tag     	|

This allows us to automatically trigger the build of two new images on Docker Hub upon drafting a new GitHub Release. The images are tagged one as `latest` (and used for deployment) and the other as the Release (for reference).
