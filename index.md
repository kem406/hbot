---
layout: default
title:  "Rob Hart's H-Bot"
---

<iframe src="https://www.youtube.com/embed/vSqIZIaWzNs"
    width="560"
    height="315"
    frameborder="0"
    allowfullscreen>
</iframe>

This drawing robot incorporates an H-Bot gantry in order to move a writing instrument across a paper sheet using only two stepper motors.

# Why use an H-Bot?

A [cartesian coordinate robot](https://en.wikipedia.org/wiki/Cartesian_coordinate_robot) normally uses 3 motors to move an end effector across an x-y plane. This can be seen on machines like the MakerBot 3D printer and the desktop version of the Shopbot.

The H-bot gantry design allows for the same x-y movement to be achieved using only 2 stepper motors. This makes the design advantageous for large-scale deployment in manufacturing, potentially lowering assembly costs, but more importantly it allows for the moving axes to be freed of carrying the weight of one of the stepper motors. Note that all motors of the drawing robot are immobile and anchored at the base - this is not something you would normally see on an x-y machine!

## How it Works

Movement on the x-y plane is completely dictated by whether the two stepper motors turn in the same direction, or rotate opposite of each other.

The left motor turning clockwise and the right motor turning counter-clockwise, for example, causes tension on the bottom of the x-axis and tension above the x-axis being loosened. This causes a net effect of downward motion.

If both motors are turning clockwise, this causes tension on the left side of the end effector to increase, while the tension on the right side relaxes. This causes a net effect of the end effector moving to the left. 

# Hardware

* Board
* Stepper motors
* Belt

<html>
    <head>
        <title>Roller</title>
    </head>

    <body>
        <div id="stl_cont" style="width:50%;height:200px;margin:0 auto;"></div>

        <script src="stl_viewer.min.js"></script>        
        <script>
            var stl_viewer=new StlViewer
            (
                document.getElementById("stl_cont"),
                {
                    zoom:50,
                    bgcolor:"white",
                    models:
                    [
                        {filename:"roller.stl", color:"#ffff00", display:"smooth", rotationx:0.5, rotationy:0.5, rotationz:0.5, animation:{delta:{rotationx:1, msec:1000, loop:true}}}

                    ]
                }
            );
        </script>

    </body>
</html>

<html>
    <head>
        <title>Pen Holder</title>
    </head>

    <body>
        <div id="stl_cont" style="width:50%;height:200px;margin:0 auto;"></div>

        <script src="stl_viewer.min.js"></script>        
        <script>
            var stl_viewer=new StlViewer
            (
                document.getElementById("stl_cont"),
                {
                    zoom:70,
                    bgcolor:"white",
                    models:
                    [
                        {filename:"penholder1.stl", color:"#ffff00", display:"flat", rotationx:0.5, rotationy:0.5, rotationz:0.5, animation:{delta:{rotationx:1, msec:1000, loop:true}}}

                    ]
                }
            );
        </script>

    </body>
</html>

<html>
    <head>
        <title>Footpad</title>
    </head>

    <body>
        <div id="stl_cont" style="width:50%;height:200px;margin:0 auto;"></div>

        <script src="stl_viewer.min.js"></script>        
        <script>
            var stl_viewer=new StlViewer
            (
                document.getElementById("stl_cont"),
                {
                    zoom:70,
                    bgcolor:"white",
                    models:
                    [
                        {filename:"footpad.stl", color:"yellow", display:"flat", rotationx:0.5, rotationy:0.5, rotationz:0.5, animation:{delta:{rotationx:1, msec:1000, loop:true}}}

                    ]
                }
            );
        </script>

    </body>
</html>

## Circuits

* [ATSAMD11 Breakout Board](https://roberthart56.github.io/SCFAB/SC_lab/Electronics/Microcontrollers/ATSAMD11/Advanced_circuits_board/index.html)

* [ATSAMD11 H-Brige Board](https://roberthart56.github.io/SCFAB/SC_lab/Output_Devices/SAMD11_stepper/index.html) x2

# Software

TBA
