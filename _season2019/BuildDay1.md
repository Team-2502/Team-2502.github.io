---
layout: post
date:   2019-01-05
title: Day 1
---
# Ideas and notes
## Key 
- **important** 
- _question_

## Vision
### Computer Vision  
#### Vision Targets
![Vision targets](https://i.imgur.com/e62fNmw.jpg)

#### Vision bitmask (by Ritik Mishra)
![Vision bitmask](https://i.imgur.com/cweadFq.png)

#### [Distorted Vision targets](https://imgur.com/a/bOwBwv4)

#### Analysis
- with one vision tape, we can tell angle of target
- with two pieces of tape, we can tell distance since there is a known distance between tape pieces (trigonometry)

also...
- slanted angle could be handy for telling height if we had a camera on an elevator, but
  1. _are we even using an elevator?_
  2. _would encoders be better? (assuming encoders are not jank like last year)_ 

## Human Vision
- We have **4 Mbps** per-team network bandwidth.
- most video cameras do not, by default, compress to the level we would want.
  - we will want a co-processor to compress the footage before we send it.
  - [reference for YouTube recommended bitrates](https://support.google.com/youtube/answer/2853702?hl=en)
- Generally **FPS > resolution**... 60FPS 420p would be optimal
- Shuffleboard does not have a full-screen camera widget
  1. _Should we make a custom Shuffleboard widget?_
  2. _Should we make a custom dashboard for a camera? (this is allowed)_
- UDP > TCP since TCP (ordered packets) causes a delay if over bandwidth whereas UDP (unordered) packets does not

### Questions
- _Should we use an Android device as the co-processor and camera?_
- _Do we want multiple human vision cameras?_ (would need switching mechanism so bitrate doesn't RIP)
- _Do we want a psuedo-birds-eye view_? (might be challenging to get working correctly)
![psuedo-birds-eye view](https://i.imgur.com/ohKuoT7.jpg)

## Autonomous

### To auton or not to auton
- **No real autonomous**. First 15 seconds drivers can still look through cameras
- A full autonomous could be marginally beneficial. It should probably not be worked on until everything else is done
-  Instead, a hybrid autonomous might make more sense
  - get close to target and have robot do fine driving to deposit item using vision tape as a reference
  - note you **can get location (x,y) of target with respect to robot** since there are two pieces of tape
  
### Completing autonomous trajectory
- Given relative (x,y) of target, we want to do a trajectory simply and quickly
  - perhaps the best way to do this is **on-the-fly computation of motion profiling splines**.
    - roboRIO might not like this. Will probably need a co-processor.
 


