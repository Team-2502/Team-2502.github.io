---
layout: post
title:  "FAQ's about build"
category: General
---
This page is dedicated to common build questions that are not covered in other pages

## Help! My screw is stripped!

You have a couple options

* Make your own head
    * Take an oscillating tool/dremel/angle grinder/whatever to the head of the bolt and create a slot
    * Use a flat head screwdriver to unscrew it
* Bolt cutters/Hacksaw
    * This will cut the bolt and disconnect the two parts without having to use an allen wrench
    * Requires that a piece of the bolt is exposed
* Pretend its a rivet
    * This involves taking a large drillbit nobody cares about and spending a few minutes drilling out the head of the bolt
    * This stops the bolt from grabbing onto one of the things that it is holding
    * This will dull the drillbit pretty badly
* Something else
    * More tips on [WikiHow](https://www.wikihow.com/Remove-a-Stripped-Screw)

## Help! My motors are stalling/struggling

You have a couple options

* Swap battery
   * If the battery is discharged or has otherwise been running for a while, it will not be able to deliver the same amount of power to the motors
   * As a result, the motors cannot deliver as much power to your mechanism
* Alter design
  * Add more motors
    * Adding more motors will distribute the load across more motors, so each motor does not have to fight/carry the load as much
    * Will also help with acceleration/deceleration
  * Counterbalance the mechanism (add a counter force)
    * Try to reduce the load by adding springs
    * Constant force springs / Spring motors are recommended for this as they will deliver constant rather than variable force
    * [Info on mounting CFS's](https://www.vulcanspring.com/blog/bid/192212/mounting-a-constant-force-spring-on-a-spool)
    * You can buy springs from Spiroflex or Vulcan Spring or wherever you find them cheap
  * Change gear/sprocket/belt pulley ratio
    * Will change the amount of torque the motor experiences
    * Less torque = motor can go faster
    
    
## Help! My auto is acting funny and code was not changed

You have couple options

* Check encoders and wires
  * If they become unplugged/sliced/removed, the robot will not know where it is
  * If the encoder light is red, then the readings are not accurate and you will need to move it closer to its magnet
* Check code for voltage-based movements
  * Voltage-based movements are unreliable and depend on battery voltage
  * Swapping them out with encoder/sensor based movements will improve consistency
* Retune PID
    * Mechanical changes (weight distribution, wheel wear, gear wear, etc) can impact robot motion parameters
    * Retuning PID/PP Lookahead/whatever can help solve these issues

## Help! My tap broke inside a hole!

You're screwed unless you have a [tap extractor](https://www.google.com/search?q=tap++extractor&safe=strict&tbm=isch)
    
