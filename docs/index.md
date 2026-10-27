---
title: Welcome
tags:
- tag1
- tag2
---
<center>
<font size= "6">Logan Maelstrom Datasheet</font><br>
as part of<br>
<font size= "8"> Drowsy Driver Alarm</font><br>
for<br>
<font size= "5"> Team 104 </font><br>

**Submission: Sept. 02 2026**
</center>

## Introduction

This datasheet documents my subsystem for a team drowsy-driver detection and alert system. The subsystem uses a (6DoF) gyroscope/accelerometer called a BMI270 IMU, and PIC18F57Q43 Curiosity Nano, to detect and process head movement associated with driver drowsiness.

### Project Summary

The Drowsy Driver Alarm project combines multiple subsystems to detect signs of driver fatigue and provide appropriate alerts. My subsystem monitors head movement using the BMI270 accelerometer and gyroscope and communicates with the team's other subsystems through the microcontroller and team interface
Additional information about the complete system can be found in the [team report.](https://asu-egr304-2026-f-104.github.io/)


### My Contribution

My primary contribution to the project is the design and documentation of the IMU subsystem. This includes integrating the BMI270 with the PIC18F57Q43 Curiosity Nano, designing a 5 V and 3.3 V power regulation circuitry, implementing the I²C interface, providing team-interface connections, and including debugging and expansion features. I also developed a subsystem schematic for the IMU and selected the supporting components required for reliable operation.
* [Block Diagram](https://logan-maelstrom.github.io/Logan-Maelstrom_EGR304_F26.github.io/01-Block-Diagram/Block-Diagram/): Provides an overview of the subsystem and its connections.
* [Component Selection](https://logan-maelstrom.github.io/Logan-Maelstrom_EGR304_F26.github.io/02-Component-Selection/Component-Selection/): Documents the major components and the reasoning behind their use.
* [BOM](https://logan-maelstrom.github.io/Logan-Maelstrom_EGR304_F26.github.io/03-BOM/BOM/): Lists the components required to construct the subsystem.
* [Schematic](https://logan-maelstrom.github.io/Logan-Maelstrom_EGR304_F26.github.io/04-Schematic/schematic/): Provides the complete electrical design and downloadable design files.
* [Power Budget](https://logan-maelstrom.github.io/Logan-Maelstrom_EGR304_F26.github.io/05-Power-Budget/Power-Budget/): Documents the subsystem's expected power requirements.
Together, these sections provide the information needed to understand, review, and continue development of my portion of the overall team system.
