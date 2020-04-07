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

There are two main benefits to the H-Bot design: cost and efficiency. The H-Bot allows for x-axis and y-axis movement using only two motors (as opposed to the three usually found on CNC machines like the desktop Shopbot or the Makerbot 3d Printer to achieve the same effect), which also eliminates the need to physically move a third motor across one of the axes.

## How it Works

TBA

# Hardware

* Board
* Stepper motors
* Belt

<!DOCTYPE html>
<html>
    <head>
        <title>Roller</title>
    </head>

    <body>
        <div id="stl_cont" style="width:20%;height:100px;margin:0 auto;"></div>

        <script src="stl_viewer.min.js"></script>        
        <script>
            var stl_viewer=new StlViewer
            (
                document.getElementById("stl_cont"),
                {
                    zoom:100,
                    bgcolor:"white",
                    models:
                    [
                        {filename:"roller.stl", display:"smooth", rotationx:0.5, rotationy:0.5, rotationz:0.5, animation:{delta:{rotationx:1, msec:1000, loop:true}}},

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
