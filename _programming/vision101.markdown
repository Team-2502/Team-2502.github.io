---
layout: post
title: Vision 101
category: Advanced
---

## Purpose

You will want to implement some sort of computer vision if
- the target/object you want to track is either
  - a distinct color (e.g yellow on a grey carpet)
  - retroreflective (so you can shine a green light at it
- the target/object is worth tracking



### What makes something worth tracking?

#### Field elements

You should only track field elements if it is hard for a human or blind (i.e no vision) autonomous routine to line up with a target, 
or if using automatic vision tracking would net you a sizeable speed advantage. For example, in 2019, it would be difficult for both a person and a blind routine to line up to place a hatch on the cargo ship.
This is contrasted with 2018, during which the field elements were large enough that computer vision would not be necessary.


#### Game elements

You should probably avoid tracking game elements. In most cases, they will be placed at consistent placces in the beginning of the match.
If your active intake requires a specific position in order to line up with the target, then you should just redesign it to be better.
Remember: "touch it, own it" should be the design mantra for an active intake. 

## Solutions

### Limelight

The limelight is an expensive but robbust solution for finding the vision target. However, it is often easy to find the target.
Most of our difficulties lie in moving towards the target. 


### Raspberry Pi 3

The RPI3 is our team's historically preferred method of tracking vision targets. Make sure to use the FRCVision image provided by
the WPILib people in order to reduce the potential of connectivity issues and increase the ability of a CSA to help you.

