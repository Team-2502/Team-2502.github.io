---
layout: post
title: Code Structure
categories: Meta
---
# Subsystems

Subsystems should go in the package `com.team2502.<year>.subsystem`. If it is a subsystem consisting multiple classes, you may make a new package inside `com.team2502.<year>.subsystem`.

# Commands

Commands not intended for use during a match such as a "reset encoders" command should go under `com.team2502.<year>.command`. Commands that are a part of autonomous groups should be in `com.team2502.<year>.subsystem.autonomous`. Autonomous command groups should be in `com.team2502.<year>.subsystem.autonomous.commandGroups`. Teleop commmands should be in `com.team2502.<year>.subsystem.teleop`

# OI

Follow the existing format in `OI.java` in `com.team2502.<year>`

1. Your Button ID should be a constant integer in `RobotMap.Joystick.Button`
2. Your Joystick should be one of the Joystick instances in `OI.java`

# Autonomous

There will be a package for autonomous "ingredients" and autonomous "recipes". In general, "ingredients" extend `Command`, while "recipes" extend `CommandGroup`.
