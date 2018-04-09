---
layout: post
title: Using Pure Pursuit
category: Pure Pursuit
---

##### WARNING: Pure Pursuit is `y`-oriented, while Motion Profiling is `x`-oriented

Alright, so you want your robot to follow a path? That can be done in 3 easy steps!

## Step 1: Define a path

### Part 1: Where to go?

This is usually achieved by measuring the field or placing points in a sketch on the carpet in the field's CAD model.
The points you place will be your waypoint, and your first waypoint will be the origin, or (0, 0). Note that if you are using
multiple Pure Pursuit commands in sequence, the waypoints will be absolute coordinates (i.e they represent distance from the position the robot was in at the beginning of auton)

### Part 2: Making waypoints in code

Now that you know where your robot will start, and where it will go, you can now make a `List` of `Waypoints`. In general, the way to do this is to put

```
public static final List<Waypoint> myPathToWinEinstein = Arrays.asList(new Waypoint(new ImmutableVector2f(0, 0), 7, 20, -7),
                                                                       new Waypoint(new ImmutableVector2f(0, 0), 7, 20, -7),
                                                                       . . .
```

in a `Paths` or `PathsConfig` class.

#### Wait, what about those constructor arguments?

1. Position
    - This is an `ImmutableVector2f` where the x-component represents left/right distance from the origin
    and the y-component represents the forward/backward distance from the origin

    - In effect, the robot starts pointing in the direction of the positive y-axis, making Pure Pursuit `y`-oriented

2. Max velocity
    - This is so that your robot doesn't go _too_ fast. If it did, it might slam into the field elements too hard and potentially cause damage.

3. Max accel
    - This is so your robot doesn't accelerate too fast. If it did, it might be sad.

4. Max decel
    - This is so it doesn't tip over.


Now, you should have a `List<Waypoint>` defining where the robot should go.

# Step 2: Using the path

Hopefully, you are using a command group to specify all the things your robot should be doing during autonomous. In the command group's constructor, type


```
addSequential(new PurePursuitCommand(myPathToWinEinstein, false))
```

substituting `myPathToWinEinstein` for the name of the `List<Waypoint>` that actually contains the path.

By the way, that second argument indicates whether or not the robot should drift at the end of its Pure Pursuit motion. By
setting it to false, it will do its best to stop at the last waypoint, rather than drifting off into the middle of nowhere.

