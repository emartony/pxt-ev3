# stop All Motors

Stops all motors currently running on the brick.

```sig
motors.stopAllMotors();
```

The motors stops but any motion caused from previously running the motors continues until it runs down. If you are driving your brick and then stop the motors, it will coast for awhile before stopping. 

## Example

Tank the @boardname@ forward at half speed for 5 seconds and then stop.

```blocks
motors.largeAB.tank(50, 50);
loops.pause(5000);
motors.stopAllMotors();
```

## See also

[stop](/reference/motors/motor/stop), 
[reset](/reference/motors/motor/reset),
[set brake](/reference/motors/motor/set-brake)