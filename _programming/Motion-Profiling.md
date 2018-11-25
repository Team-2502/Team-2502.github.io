---
layout: post
title: Motion Profiling (Old)
category: Old/Deprecated
---
# This wiki page is a work in progress

# Using Motion Profiling for autonomous

If you want smooth robot motion, use this. It's super repeatable, even if your battery voltage changes or if your robot got fat.

For Voyager, the robot had the following values:

Average time to max speed (low gear): `0.8282773189 seconds`

Average max speed in RPM (low gear): `557.6 RPM`

Average max speed in NU/100MS (low gear): `3781.457 Native Units / 100 milliseconds`

Appropriate Feed Forward gain: `0.27053062082237783`

Average max speed in FPS (low gear): `9.731955898 ft / second`

Average max acceleration in G (low gear): `0.3784 G`

Average max acceleration in ft/s^2 (low gear): `12.1088 ft/s^2`

Some helpful resources because this resource is unhelpful

* [CANTalon Motion Profile Reference Manual](https://content.vexrobotics.com/vexpro/pdf/217-8080-Talon-SRX-Motion-Profile-Reference-Manual-20160119.pdf)

* [A handy dandy spreadsheet that goes along with the above manual, specifically section 6](https://github.com/CrossTheRoadElec/FRC-Examples/blob/master/Motion%20Profile%20Generator.xlsx)
