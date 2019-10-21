---
layout: post
title: GitHub Workflow Description
category: 
---
# Branching

There are only 3 types of branches:

* `master`

* `develop`

* `feature-` 

## master branch

This branch *needs* to be confirmed working. You are only allowed to merge into this branch from `develop` via pull request. You are *not allowed* to merge untested/unfinished/non-functional code. *NEVER* push directly to this branch.  

## develop branch

This branch should work. You are allowed to directly push small changes to this branch, however you should make sure that what you have written works and has been tested on an actual robot. *DO NOT PUSH UNTESTED CODE TO THIS BRANCH.* If you are not sitting near the robot with the intent to test your code very soon you should probably consider creating a feature branch instead. You are allowed to merge any branch into this branch via pull request.

Small changes include, but are not limited to:

* Changes to Motor ID's in RobotMap

* Changes to OI mappings

* Formatting changes

## feature- branches

ex: feature-intake, feature-vision

These are branches for major changes/new features. These generally include:

* New subsystems (no matter how big/small) and commands that go with them

* Large projects such as path-following autonomous, automatic shifting, vision changes, etc.

* Major updates to an existing subsystem

If your code changes include new files you should probably consider making a feature branch.
You can merge any branch into these branches


# Deploying

At competition or other event where the robot is being driven,

* On practice day, code from the `master` branch is deployed, unless `develop` has significant improvements.

    * If problems are found in `develop` and they cannot be fixed, deploy from `master` instead.

* If code changes are required at an event, follow this plan

![Flowchart](https://i.imgur.com/TU2piBi.png)
