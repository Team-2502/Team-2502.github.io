---
layout: post
title: Logging
categories: General
---

Logging is a useful way to see which parts of your code are running at what time. 
There are two ways to log info, both of which will show up on the driver station.


## Method 1: System.out.println

This is the more common of the two methods. Just call `System.out.println` from somewhere in your code,
and it will show up somewhere on the driver station console as long as you have enabled all print outs.

## Method 2: Static methods of DriverStation

Alternatively, if you want to print an error or warning, you will have to use the static methods in the `DriverStation` class. They are

* `reportError` 
* `reportWarning`

You can find more info about them in the WPILib JavaDoc [here](http://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/DriverStation.html#reportError-java.lang.String-boolean-)
