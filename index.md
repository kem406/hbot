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

## How it works

Movement on the x-y plane is completely dictated by whether the two stepper motors turn in the same direction, or rotate opposite of each other.

The left motor turning clockwise and the right motor turning counter-clockwise, for example, causes tension on the bottom of the x-axis and tension above the x-axis being loosened. This causes a net effect of downward motion.

If both motors are turning clockwise, this causes tension on the left side of the end effector to increase, while the tension on the right side relaxes. This causes a net effect of the end effector moving to the left.

A more rigorous mathematical model of the H-Bot's movement can be found [here](https://www.icvr.ethz.ch/ConfiguratorJM/publications/MODELING_A_132687166151936/3314_mod.pdf).

The crisscrossing of the drive belt is not necessary for the H-bot design, though it greatly stabilizes the wobbliness of the x-axis.

# Hardware

## Circuits

* [ATSAMD11 Breakout Board](https://roberthart56.github.io/SCFAB/SC_lab/Electronics/Microcontrollers/ATSAMD11/Advanced_circuits_board/index.html)

* [ATSAMD11 H-Brige Boards](https://roberthart56.github.io/SCFAB/SC_lab/Output_Devices/SAMD11_stepper/index.html)

## 3D-printed hardware

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

### Rollers

The rollers used for this robot were designed by Jake Read for the machine design portion of MIT's How to Make Almost Anything class. More information can be found [here](https://gitlab.cba.mit.edu/jakeread/machineweek-2019). The stl for the roller itself can be downloaded [here](https://kem406.github.io/hbot/roller.stl).

### End effector

The end effector was designed to hold a pen-sized marker which fits through the shaft. Two small rectangle-shaped reliefs were incorporated into both ends of the end effector—these are designed to snugly contain (with a small application of superglue) a small cut-off portion of the drive belt.

[<img src="ee1a.jpg" alt="ee1a">](https://kem406.github.io/hbot/ee1b.jpg)

These embedded bits of drive belt can then act as the "teeth" that holds the main drive belt in place.

[<img src="ee2a.png" alt="ee2a">](https://kem406.github.io/hbot/ee2b.jpg)

With a 3d-printed fastener (.stl can be downloaded [here](https://kem406.github.io/hbot/fastener.stl)) and some M3 screws and washers, the main drive belt can be fastened on top of the "teeth."

[<img src="ee3a.jpg" alt="ee3a">](https://kem406.github.io/hbot/ee3b.jpg)

The end effector was designed to allow two M3 nuts to be embedded snugly in place for this purpose. Two more M3 nuts can be fitted inside two slots towards the top of the end effector; this allows for future additions (such as a solenoid) to be bolted on top.

The .stl file for the end effector can be downloaded [here](https://kem406.github.io/hbot/penholder1.stl).

### Footpads

These hourglass-shaped footpads are nothing special and exist entirely to support the back end of the robot. The .stl file for the footpads can be downloaded [here](https://kem406.github.io/hbot/footpad.stl).

## Miscellaneous hardware (non-exhaustive)

* Fiberglass board
* M3 hardware
* Drive belt
* [Unipolar stepper motors](https://www.jameco.com/z/42BYGH404-R-Unipolar-Stepper-Motor-12VDC-400mA_238538.html)
* 12-volt power supply


# Software

TBA
