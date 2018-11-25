---
layout: post
title:  "Gears, Sprockets, and Belts"
category: General Mechanics
---

So you want to transfer rotational motion? You have 3 options at your disposal: gears, sprockets, or belts

# Gears

Gears are heavy yet robust. They usually come in gearboxes, and it is possible to have [multiple-speed transmissions](https://www.vexrobotics.com/wcp-ds.html) when you use gears. 

We use gears for applications where it cannot fail, such as when building drivetrains and climbers. 

## Gear ratios

Gear ratios are an easy way to ensure that your motors don't stall out when you try climbing or something like that. They are important to think about when designing a drivetrain.

### Gear ratio notation

Gear ratios come in the form of `driver gear:driven gear`. For example, if I have a gear ratio of `2:1` (or `2`), it will take 2 revolutions on the input for every 1 revolution on the output. This means that the output will rotate half as fast as the input, and the torque will be doubled. 

### Gear ratio physics

A gear ratio that is greater than 1 maximizes the amount of torque that is output. In contrast, a gear ratio that is less than 1 maximizes the speed of the output gear. By increasing torque, you increase the amount of force required to slow/stop the gears. By increasing speed, you go faster.

When picking a 2-speed drivetrain, it is conventional for us to pick a "high gear ratio" (less than 1) and "low gear ratio" (greater than 1). 


# Sprockets

Sprockets are heavier yet stronger than belts. They are messy (in that they are greasy), and can be hard to install if the sprockets are in a tight spot.
This is because installing chain on sprockets generally requires the use of a master link, which often pops off and gets lost as you are trying to install it.

If you pretend the robot is a bicycle and install a derailleur, you are officially crazy and should _really truly for real_  be using gears instead.

There are 2 kinds of chain: #25 pitch and #35 pitch. #25 pitch chain is smaller, weaker, and lighter, while #35 pitch is larger, stronger, and heavier. Use #35 pitch chain in applications where strength 
matters, such as the drivetrain and climbers.

Keep in mind that you must have an integer number of chain links in order to have properly tensioned chain. By properly tensioning your chain, you ensure that there is little to no backlash in the system (backlash is when you can rotate 1 sprocket/gear without moving the other sprocket/gear when the two are connected). To calculate the number of chain links you will need to use, you can use the following equation.  

{% comment %} 
![Chain Equation](https://i.imgur.com/rIH5xBA.png)
{% endcomment %} 


{% raw %} 
$$ C = \frac{2d}{E_1} + \frac{E_2}{2} + \frac{E_3}{2} + \frac{\left( \frac{E_2 - E_3]{2\pi} \right)}{\frac{d}{E_1}}$$
{% endraw %} 

In this equation, C is the number of chain links you will need, E1 is the chain pitch in inches (for #35, it is 0.375 inches, for #25, it is 0.25 inches), E2 is the number of teeth on one sprocket, E3 is the number of teeth on the other sprocket, and d is the center-to-center distance between the sprockets. Generally, you will 

1. Put the sprockets down in the CAD somewhere
1. Compute the chain equation
1. Solve for d when C is rounded up/down
1. Move the sprockets in the CAD



# Belts

Belts lightweight and easy to install. However, they come in fixed sizes, requiring you to design around them. As long as you *CAD the robot*, this should
not be an issue. 

There are 2 types of [belts](https://www.vexrobotics.com/vexpro/motion/belts-and-pulleys) that you will probably use: HTD, and GT2. HTD belts have a larger, more coarse profile while the GT2 belts are smaller.



If your belts keep snapping/slipping, it is time to consider upgrading to sprockets.
