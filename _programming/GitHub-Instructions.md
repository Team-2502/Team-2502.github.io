---
layout: post
title: GitHub Workflow Description
category:
---
# Branching

Since 2017, you are *not* allowed to have a personal branch. Any such branch will immediately be deleted. There are only 3 types of branches:

* `master`

* `develop`

* `feature-` branches

## master branch

This branch *needs* to be confirmed working. You are only allowed to merge into this branch from `develop`. You are *not allowed* to merge untested/unfinished/non-functional code. *NEVER* push directly to this branch.  

## develop branch

This branch *ideally* works. You are allowed to directly push small changes to this branch. You are allowed to merge any branch into this branch. If you are merging `master` into this branch, something has gone very, very wrong.

Small changes include, but are not limited to

* Changes to Motor ID's in RobotMap

* New autonomous groups

* Formatting changes

## feature- branches

These are branches for large changes/new features. These generally include

* New subsystems (no matter how big/small) and commands that go with them

* Large projects such as path-following autonomous, automatic shifting, vision changes, etc.

* New files directly under `com.team2502.robot2018` such as `AutoSwitcher`

You can merge any branch into these branches, and you can merge these branches into any other branch, *barring* `master`.


# Deploying

At competition or other event where the robot is being driven,

* On practice day, code from the `master` branch is deployed, unless `develop` has significant improvements.

    * If problems are found in `develop` and they cannot be fixed, deploy from `master` instead.

* If code changes are required at an event, follow this plan

![Flowchart](https://i.imgur.com/TU2piBi.png)
