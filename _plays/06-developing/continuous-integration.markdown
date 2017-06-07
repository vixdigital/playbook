---
title:  "Continuous Integration"
categories: developing
---

Continuous Integration (CI) is an important part of our workflow at VIX. Essentially CI is a practice that involves merging our code into a shared repository continuously throughout the day. For us, this means we all merge our changes into a *latest* branch.

Before each change gets merged in it is put through our automated build and test pipeline which will flag up any breaking changes and allow us to ammend them quickly before trying again. 

If our changes pass their initial pipeline run they are merged in to latest which is itself run through the pipeline to make sure it still works post-merge.

In summary, some the benefits of adopting a CI workflow are:
- Reduces the chance of major integration problems by catching smaller conflicts often and not allowing them to build up
- Increases development visibility within the team
- Goes hand in hand with Continuous Deployment, making sure the latest stable changes get into production as soon as possible

Some of the tools we use for CI are:
- [GitLab CI & CD](https://about.gitlab.com/features/gitlab-ci-cd/)
- [Slack](https://slack.com/) hooks for notifications of pipeline failures