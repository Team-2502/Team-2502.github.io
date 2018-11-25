---
layout: post
title: Deploying to a roboRIO with a password
category: Old/Deprecated
---

This talks about the antiquated Ant build system, which was phased out in 2019. 

A password has been set on the RoboRIO. This makes it so that, with the default build configuration, it is impossible to deploy. However, this is an easy problem to fix for the time being.

## Step 1: Open build.properties
The first step is to edit build.properties. This build.properties is found in `$HOME/wpilib/java/current/ant/build.properties`, where `$HOME` is your home folder.  Open up the file in a text editor.

## Step 2: Add the password
Currently, line 5 should read

    adminPassword=

Change it to read

    adminPassword=team2502

This allows the deploy process to use the password to SSH into the roboRIO.

## What to do when Donovan removes the password

Do step 1 and revert the change made in step 2

## How to remove password from RoboRIO

Re-image the RoboRIO. Preferably, you'd get an experienced person to do it for you if you are not experienced. If you aren't, and go ahead with it anyways, and brick the RoboRIO, it's ok. We can fix a bricked RoboRIO. Make sure to go to ScreenSteps for instructions!
