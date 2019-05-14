---
layout: post
title: An Introduction to Moving Things Upwards
categories: Vertical Motion
---

Often times, an FRC game will require that you pick an object off of the floor (power cube, grey tote, inflatable tube, cargo ball, hatch panel),
and place it somwhere (peg, scale plate, tote stack, rocket, etc). Sometimes, such as in 2018, you are able to get away with not having an 
elevator by either only doing the low goal, or shooting. This document outlines several methods of placing an object up high

## Elevator

An elevator is probably the most obvious way to move something up high, and is within the team's limits. There are several design considerations
that you will want to make when designing an elevator

### Continuous vs Cascading

A continuous elevator will move one stage up at a time. This has the advantage that your center of mass is never higher than it needs to be, but
it is slower than a cascading elevator, which moves all stages up at once. Additionally, it is mildly harder to string a cascading elevator together.
Daedalus (our 2018 robot) and the Cheesy Poof's (team 254) 2018 robot provide examples of a continuous elevator.


A cascading elevator moves all the stages up at once. This is much faster, and can be easier to string together. It is also easier to counterbalance,
since the amount of load on your motors is more or less constant (excluding weight increases/decreases from picking up/releasing game pieces)
The 2018 robot from Simbotics (team 1114) is an example of a continous elevator. It is 

### Passthrough/Pass behind

Sometimes, the setup of the field can allow for cycles to be marginally faster if your robot is able to pass game objects from the front 
to the back. For example, in 2018, if you were facing the cubes that were against the switch on the platform side, the scale would be behind
you. 

#### Pass Through

This means that your wristed active intake is able to rotate through the elevator. This requires an elevator that is sufficiently wide that has its
strings routed through the tubes on the sides. For example, it would be extremely difficult to create a pass through for Daedalus, since its up rope goes right 
through the middle of the space between the two sides. 

Some good examples of a pass-through include:

- 5190 from 2019
- 254 from 2018
- 1678 from 2019

#### Pass Over (not the holiday)

Sometimes, you may only wish to move pieces from the front to the back when your elevator is at its maximum extension height (or in the case of a 
continuous elevator, at stage boundaries). This will require a relatively thin elevator with a long wristed active intake, so that at the top, the wrist
can rotate 180 degrees. It is hard to describe in words, but some good examples include
- 195 from 2018
- [1619 from 2018](https://youtu.be/k3w4hPvwMqI?t=36)

#### Bearings

You will need to place bearings strategically in order to reduce friction (grease is a bad idea; it will get everywhere).
See [the 973 guide to an elevator](https://www.youtube.com/watch?v=wZ6a6dc4BGg) to learn more about bearing blocks and elevators in general.


##### Buying tiny circle bore bearings

Bearings are a very often used part in many industries. You could buy them off of McMaster, but other places sell tiny bearings that are a little cheaper, such as [vxb.com](http://vxb.com). A .25" bore will easily slide onto a 1/4-20 bolt or an appropriate shoulder bolt (#10-24 with a 1/4 inch shank). In contrast, a 3/16" bore will be an extremely tight fit onto a #10-32 bolt. You may need to sand 1 or 2 thou off the bolt diameter to get it to fit. 


#### Counterbalancing

You should use a constant force spring for an elevator. If you are using a continuous elevator, you may need one (or two, to apply force evenly to both sides and avoid applying
a torque) CFS's per stage. You can buy them from Vulcan Spring, and in 2018, they offered 6 free springs per FIRST, so check to see if they still have that before paying
cash.

#### Misc. tips

- If possible, attach the string to the metal parts using inline spri

## Arm

An arm is probably not within our team's limits. We have not done a big arm before. Good examples of arms include 971 from 2018. Okay
examples of arms include 3750 from 2019. The difference is completely in the software; 971 automated as much of their arm as they could.
Meanwhile, Gator Robotics (it appears) simply allowed the driver to directly control the position of both joints.

#### Counterbalancing.

The magnitude of the force exerted by gravity in the direction perpendicular to the arm is

{% raw %} $$ F = mg \cos{\theta} $$ {% endraw %}

given {% raw %} $$ \theta $$ {% endraw %} is the angle of the arm from the horizontal, and so the torque exerted by gravity on the arm will be

{% raw %} $$ \tau = mg d \cos{\theta} $$ {% endraw %}

where {% raw %} $$ d $$ {% endraw %} is the distance of the center of mass of the arm from the pivot (you can use CAD to figure this out; just make it detailed)

Therefore, to properly counterbalance the arm, you will likely need software-based motor control (put an encoder on the rotation shaft!!) in addition to
mechanical counterbalancing. Note that a typical coil spring/gas shock will increase the amount of force it exerts linearly with respect to how much it is extended,
so you should use it over a constant force spring. Just make sure that your spring constant (spring stiffness, units are in newtons/meter or pounds/feet) isn't too high; you want precise control of the arm, not a situation where the spring pulls the arm back when it is almost upright. 

Don't be afraid to use physics (i.e free body diagrams) to help you in this respect. It will drastically improve the build quality.



#### Pink Arm

A pink arm is an arm that also can extend out. It is named after the Pink Team (233) who built them often in the mid 2000's. Some good recent examples
include 610 from 2019 and 2481 from 2018.

This is certainly not within our team's limits.

