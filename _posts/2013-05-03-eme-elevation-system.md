---
id: 2676
title: 'EME Elevation System'
date: '2013-05-03T00:24:41+00:00'
author: 'Gavin, M1BXF'
layout: post
guid: 'http://dx.camb-hams.com/?p=2676'
permalink: /2013/05/03/eme-elevation-system/
video_type:
    - '#NONE#'
categories:
    - General
tags:
    - mull2013
---

So progress is being made on the elevation system. We have the mechanical side complete, the controller/feedback had some issues but a solution is now sorted.

## Mechanical

[![2013-04-19 22.22.29](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-04-19-22.22.291_thumb1.jpg "2013-04-19 22.22.29")](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-04-19-22.22.2911.jpg)

You can see the milled and turned pieces of metal Dave M0VMC has produced for us. Dave was on the 2008 DX’Pedition and has access to a wide range of tools.

The left round bar fits in the top of the [Flossies](http://www.camb-hams.com/flossie) mast with the 2 smaller bits forming a hinge when assembled (see left photo below), the larger bar is the lower Jackarm mount (see right photo below). The Jackarm attaches between this lower bracket and a similar bracket attached on the upper pole where the antenna also mounts. This means when the Jackarm extends then pole the antenna mounts on is forced to move at the hinge point and thus you have elevation.

[![P1030288](http://dx.camb-hams.com/wp-content/uploads/2013/05/P1030288_thumb.jpg "P1030288")](http://dx.camb-hams.com/wp-content/uploads/2013/05/P1030288.jpg) [![P1030289](http://dx.camb-hams.com/wp-content/uploads/2013/05/P1030289_thumb1.jpg "P1030289")](http://dx.camb-hams.com/wp-content/uploads/2013/05/P10302891.jpg)

## Control and Feedback

This was always going to be the challenge, you can see how much fun it was testing a few options by this photo

[![2013-04-25 22.54.15](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-04-25-22.54.151_thumb2.jpg "2013-04-25 22.54.15")](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-04-25-22.54.1512.jpg)

There are 3 ways we could get elevation position feedback

1. The Jackarm has a reed-switch and magnet in it which gives 1 pulse per revolution, count the revolutions for 0 to 90 degrees and you can calculate the position.
2. Attach a potentiometer somehow to the hinge so we know the mechanical position of the hinge
3. Use an accelerometer like the one [Gavin M1BXF used](http://www.geekshed.co.uk/picaxe-18m-mxd2125-based-elevation-module/) for his own EME system.

Each of these systems have advantages and disadvantages.

### Option 1 – Jackarm Rotation Pulse

There are 2 disadvantages to this option. First, due to geometry this system is non-linear. When at 0 degrees (everything a right angles, right photo of the system on the grass above) an extension of the jackarm by 1 inch will say be 1 degree, but at 45 degrees or so then an inch of the jackarm might only be 0.5 degrees. This can be calibrated out in code or a custom analogue meter scale. The second issue is of the system is powered off when not at 0 degrees the when powered back up there is no way to know the angle and so the antenna must be elevated back down to 0 degrees to get a known position.

### Option 2 – Potentiometer

This would have been the best option, 0v on one side, 5v on the other and the wiper to an analogue meter. However we would have had to machine the metal to allow mounting a potentiometer which we never done, maybe in rev 2 ![Smile](http://dx.camb-hams.com/wp-content/uploads/2013/05/wlEmoticon-smile.png)

### Option 3 – Accelerometer (MXD2125)

This is a known working design but needed modification to allow displaying the position as previously it was connected into a G6LVB rotator interface which only needed an analogue voltage. In reality this was just a little bit of extra code which overall **turned out to be the best option**.

[![2013-05-03 00.08.33](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-03-00.08.33_thumb1.jpg "2013-05-03 00.08.33")](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-03-00.08.331.jpg) [![2013-05-02 23.01.45](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-02-23.01.451_thumb1.jpg "2013-05-02 23.01.45")](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-02-23.01.4511.jpg)

This system will be made up of 3 elements, a box to control the Jackarm motor which is 12v, the outside box housing the MXD2125 accelerometer + PIXACE-18X chip which attaches to the pole above the Jackarm near the antenna and the display unit.

[![2013-05-02 23.56.01](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-02-23.56.011_thumb1.jpg "2013-05-02 23.56.01")](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-02-23.56.0111.jpg) [![2013-05-02 23.11.04](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-02-23.11.041_thumb1.jpg "2013-05-02 23.11.04")](http://dx.camb-hams.com/wp-content/uploads/2013/05/2013-05-02-23.11.0411.jpg)

The Jackarm extends or retracts by simply reversing the polarity on the motor.

A video showing the final assembly in action;

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" loading="lazy" src="https://www.youtube.com/embed/7rOxj-GvW7I" width="560"></iframe>

Gavin, M1BXF.