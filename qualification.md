---
layout: page
title:  "Qualification"
---

Our ultimate goal is to

<div class="alert dark">Provide superior quality software that meets or exceeds user requirements and expectations.</div>

Therefore, the process we put in place must be capable of consistently producing software with the level of quality we aim for. The best way to achieve so it is to build quality into the process itself. To accomplish that, we follow the principles below.

- Automate all repetitive tasks.
- Leave to human judgment critical decisions.

Automation is essential for executing repetitive tasks, such as running the test suite, checking coding style or drafting a release, in a fast and predictable way eliminating any possible error or omission due to humans. However, human judgment can't be replaced (yet) for operations which require decision making such as [issue approval](https://inforlife.github.io/process/issues.html#approval), [code review](https://inforlife.github.io/process/code-review.html), or [issue acceptance](https://inforlife.github.io/process/iterations.html#user-acceptance).

The balance we have achieved between humans and machines guarantees each piece of software we run in production

- It passes an extensive set of automated tests which verify its correctness.
- It conforms to our coding style.
- Its design was approved by a team member.
- All released issues were approved by our QA (or confirmed by the development team) and accepted by the users who requested them
- [It was successfully packed](https://inforlife.github.io/process/release.html#image-build) with all the dependencies it requires to run properly.

Thanks to the restrictions we have in place we can reduce the scope of qualification and, to qualify a new deployment, perform the simple checks below.

- A Standard Operating Procedure including the "procedural" aspects[1](#notes) of the application was released.
- The application stack[2](#notes) was successfully deployed to the production environment.
- The application booted without any errors.

Due to our process, we think it is more appropriate to merge aspects traditionally divided into different protocols (IQ/OQ) into a single Qualification Protocol which provides documented evidence of all the aspects listed above.


Moreover, by separating the protocol from the report, we don't need to issue and approve a new protocol before a new deployment.

It is enough to create, from the approved master, a new test report where we document the successful deployment. Since qualification takes very little time, we can deploy more often providing valuable software to users more quickly.

Since our test and production environment are virtually identical, we may assume if an application performs as expected when undergoes testing, it does the same under real-world conditions. Thus, we don't execute any Performance Qualification after deploying a new release to the production environment.


#####Notes:
1. All the aspects related to the usage of the applications are included as source code and checked into the project repository. They are published as documentation website available at https://inforlife.github.io/doc-REPOSITORY.
2. The application stack is the set of all pieces of software required to run the entire application, from the operating system to the code we wrote.
