# Red Light, Green Light

## Introduction @fullscreen

Use the ``||sensors:pause color sensor||`` block to play Red Light, Green Light with your @boardname@ robot! 

![Brick simulation with color sensor and motors](/static/tutorials/redlight-greenlight/redlight-greenlight.gif)

## Step 1

Open the ``||sensors:Sensors||`` Toolbox drawer. Drag out **2** ``||sensors:pause color sensor||`` blocks onto the Workspace, and drop them into the ``||loops:forever||`` loop.

```blocks
forever(function () { 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Blue) 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Blue) 
}) 
```

## Step 2

In the first ``||sensors:pause color sensor||`` block, use the second drop-down menu to select the "Green" color.  In the second ``||sensors:pause color sensor||`` block, use the second drop-down menu to select the "Red" color. 

![Color selection dropdown](/static/tutorials/redlight-greenlight/pause-color-sensor-dropdown.png)

```blocks
forever(function () { 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Green) 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Red) 
}) 
```

## Step 3

Open the ``||motors:Motors||`` Toolbox drawer. Drag out a ``||motors:tank large motors||`` block onto the Workspace, and drop in between the ``||sensors:pause color sensor||`` blocks.

```blocks
forever(function () { 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Green) 
    motors.largeBC.tank(50, 50) 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Red) 
}) 
```

## Step 4

Open the ``||motors:Motors||`` Toolbox drawer. Drag out a ``||motors:stop all motors||`` block onto the Workspace, and drop it in after the second ``||sensors:pause color sensor||`` block in the ``||loops:forever||`` loop.

```blocks
forever(function () { 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Green) 
    motors.largeBC.tank(50, 50) 
    sensors.color3.pauseUntilColorDetected(ColorSensorColor.Red) 
    motors.stopAll() 
})
```

## Step 5
 
Now, plug your @boardname@ into the computer with the USB cable, and click the **Download** button at the bottom of your screen. Follow the directions to save your program to the brick.

Attach a Color Sensor to Port 3 of your brick, and attach your brick to a driving base with large motors attached to Ports B and C. See the building instructions for: _Driving Base with Color Sensor Forward_. Test your program by putting a green or red piece of paper or LEGO brick in front of the color sensor.