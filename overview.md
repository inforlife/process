---
layout: page
title:  "Overview"
---

At ACS Dobfar Info SA we have structured our process around [GitHub](https://github.com/). Thanks to all the available integrations, GitHub allows us to centralize the entire life cycle around a single product providing all the traceability information we need while keeping the process fairly easy to follow.

All the source code is managed using [Git](https://git-scm.com/), a distributed version control system that keeps track of all the changes made during the application's live. Git comes with the concept of *branches*, a branch represents an independent line of development. They may be seen as a way to create a brand new working directory and project history.

We adopt a slightly modified version of what it is known as [GitHub Flow](https://guides.github.com/introduction/flow/) to organize how features are implemented.

Each project comes with two long-lasting branches that live for the entire span of project. The **master** branch contains the code currently running in production, while the **development** branch contains the code ready to be shipped to production. In addition to those branches, many feature branches (one for each implemented feature) are created right before starting to implement a feature and deleted once the feature is 'done'.

We have currently divided our process into five main steps.

- [**Setup**](http://acsinfo.github.io/process/setup.html) - The activities performed by the team to  properly configure all the tools used to manage the project.
- [**Gathering**](http://acsinfo.github.io/process/gathering.html) - The activities performed by the team and stakeholders to manage the list of functionalities stakeholders wish the applications have.
- [**Development**](http://acsinfo.github.io/process/development.html) - The activities performed by the team from the checkout of a feature to its completion.
- [**Release**](http://acsinfo.github.io/process/release.html) - The activities performed by the team to deploy a set of completed features to production.
- **Operations** - The activities performed by the team to manage the applications once running in production (including the infrastructure the applications rely on).
