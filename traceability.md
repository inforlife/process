---
layout: page
title:  "Features Traceability"
---

Traceability of a feature in the source code is fulfilled thanks to the branching strategy used by the development team. Each feature (user story) is implemented in a dedicated branch that is merged into the mainstream through a GitHub pull request. The reference to the PR is included in the GitHub issue containing the user story so for each feature is always possible to pinpoint the code that has implemented it. 

# Completeness    

To ensure a feature is implemented in its totality, each feature comes with a specific RSpec `integration test`[1](#notes).

The integration test is named after the user story title it refers to. 

The integration test contains a scenario for each condition of satisfaction listed in the GitHub issue.


#####Notes:
1. According to the type of application and feature, this may be a feature spec, a request spec or some other kind of end-to-end specification.  