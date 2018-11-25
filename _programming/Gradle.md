---
layout: post
title: Gradle
category: Deploy
---

As of the 2019 FRC season, Gradle is now officially supported over the old Ant-based system. 

# Gradle
[Gradle](http://gradle.org/) is a build assistant which has the ability to streamline the build process by running multiple tasks on build (e.g. Compiling the Code, Creating JavaDoc, Pushing Jars to Download Page. All in one command) as well as interfacing with maven to easily download dependencies.

## Gradle info
If you have not [Setup Java](https://github.com/Team-2502/RobotCode2017/wiki/Java) do that now.  
The terminal command to run Gradle differs based on your OS
* Windows:
  * `gradlew`
* OSX & Linux:
  * `./gradlew`
  
Use the appropiate choice when executing these commands.  

Run `gradlew tasks` for information on the possible tasks to run with gradle.  

### Opening command line on Windows

To access a directory through the command line on Windows open directory in explorer and `Shift + Right-Click` and select `Open command window here.

### Opening command line on Mac

Run `/Applications/Utilities/Terminal.app` and `cd` into the directory.


## Setup
Clone this project using either the `git` command line tool or [Github Desktop](https://desktop.github.com/).  

Open the directory of the robot code from the command line and run `gradlew eclipse` to prepare the project for the Eclipse environment or `gradlew idea` to prepare for the Intellij Idea environment.

### Importing into IntelliJ Idea
Import the project from Gradle. IntelliJ can then set up the project.

## Build
Open the directory from the command line and run `./gradlew build` on OSX/Linux or `gradlew build` on Windows

## Deploy
Open the directory from the command line and run `./gradlew deploy` on OSX/Linux or `gradlew build` on Windows
