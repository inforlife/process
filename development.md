---
layout: page
title:  "Development"
---

When a developer starts working on a new feature, right after creating the empty branch he opens in GitHub a [pull request](https://help.github.com/articles/using-pull-requests) to merge the feature branch into **development**. This is helpful as everyone can see what the other members of the team are working on by simply checking all the open pull requests.

At every push to GitHub the feature branch goes through [CI](http://acsinfo.github.io/process/ci.html) to ensure the new code didn't break anything.

When completed, the feature must be reviewed before it can be merged into **development**. So, the developer marks the pull request as *ready for review* and assigns it to another member of the team.
As soon as possible, the reviewer looks through the pull request and adds comments where necessary.

Once the review is completed, developer and reviewer meet (physically or remotely) and complete the review by going together through the comments.

If the pull request contains any code that requires refactoring, it is updated according to the code review before the branch is merged into **development** (and the issue marked as *reviewed*). Otherwise, the merge can be done as soon as the review is completed.

We believe that code review is the single biggest thing we can do to improve the quality of the code we produce and, as very positive side effect, it also improves developers' skills.

Note that code review may be skipped for features developed through [pair programming](https://en.wikipedia.org/wiki/Pair_programming).

To make sure nobody introduces changes into production without review, we have defined the following rules.

1. Nobody can never merge their own feature branches (this rule is not enforced through technology, but as team policy).

2. Nobody can add code directly neither to **master** nor to **development**, but only through the merge of a pull request (this rule is enforced through technology with the use of Git hooks).
