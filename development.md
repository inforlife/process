---
layout: page
title:  "Development"
---

When a developer starts working on a new feature, right after creating the empty branch he opens in GitHub a [pull request](https://help.github.com/articles/using-pull-requests) to merge the feature branch into **master**. This is helpful as everyone can see what the other members of the team are working on by simply checking all the open pull requests.

At every push to GitHub the feature branch goes through [CI](http://acsinfo.github.io/process/ci.html) to ensure the new code didn't break anything.

When completed, the feature must be reviewed before it can be merged into **master**. So, the developer assigns the pull request to a  *reviewer* (another member of the team).
As soon as possible, the reviewer looks through the pull request, adds comments where necessary, and, according to the outcome of the review, approves it or requests changes.

Once the review is completed, developer and reviewer meet (physically or remotely) and complete the review by going together through the comments.

If the pull request contains any code that requires changes, it is updated according to the review before the branch is merged into **master** (and the issue marked as *reviewed*). Otherwise, the merge can be done as soon as the review is completed by the branch owner.

We believe that code review is the single biggest thing we can do to improve the quality of the code we produce and, as very positive side effect, it also improves developers' skills.

Note that code review may be skipped for features developed through [pair programming](https://en.wikipedia.org/wiki/Pair_programming).

To make sure nobody introduces changes into production without review, we have defined the following rules.

1. Nobody can add code directly to **master**, but only through the merge of a pull request.
