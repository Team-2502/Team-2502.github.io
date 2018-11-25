---
layout: post
title: Motors and Pneumatics
category: WPILib
---
# Talons
First, import `com.ctre.phoenix.motorcontrol.can.WPI_TalonSRX`

To create a talon:

`WPI_TalonSRX someTalon = new WPI_TalonSRX(RobotMap.Motor.SOMETALON)`

Instantiate the CANTalon class, passing in an `int` for the Talon ID into the constructor. Please put this `int` in `RobotMap.Motor` so that we can easily check what the talon ID's are supposed to be.

To drive a talon

`someTalon.set(controlMode, value)`

`amount` does different things based on what `controlMode` is.

For more details, look at the CANTalon javadoc at [this URL](http://www.ctr-electronics.com/downloads/api/java/html/com/ctre/phoenix/motorcontrol/can/WPI_TalonSRX.html).

# Solenoids

First, import `edu.wpi.first.wpilibj.Solenoid`

To create a talon:

`Solenoid balloon = new Solenoid(RobotMap.Solenoid.SOMESOLENOID)`

Instantiate the Solenoid class, passing in an `int` for the Solenoid ID into the constructor. Please put this `int` in `RobotMap.Solenoid` so that we can easily check what the solenoid ID's are supposed to be.

To move a pneumatic

`balloon.set(boolean)`

`boolean` indicates whether the pneumatic is activated or not.


For more details, look at the Solenoid javadoc at [this URL](http://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/Solenoid.html).
