..    include:: <isonum.txt>
.. contents:: Build Manual

Build
==================


Miscellaneous
------------------------

(1) Laptop with Ubuntu Xenial 16.04.01 LTS installed. (Other versions of Ubuntu may work as well, but we can’t guarantee this.)

The Hardware Kit
----------------------------
Mechanical
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(1) Traxxas RC rally car (recommended model: Ford Fiesta ST)
Note: as of August 2018, this car is sold with a brushed motor by Traxxas. See link below for brushless motor.
(1) Velineon 3351R/3500 brushless DC motor
(1) laser-cut chassis on which you will mount everything
(1) LIDAR mount with (2) C-shaped brackets
(2) threaded 14mm M3 standoffs
(4) 19mm M3 standoffs
(8) 35mm M3 standoffs
(4) 45mm M3 standoffs
(35) 10mm M3 screws
(4) 20mm M3 screws
(4) 8mm round nylon spacers
(1) Roll of double-sided tape (for mounting USB hubs and optionally FOCbox)


Electrical
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(1) power board (obtained from University of Pennsylvania team. This was designed at Penn, printed by ​www.4pcb.com​)
(1) Nvidia Jetson TX1 or TX2 with Wi-Fi antennas (included with the development board)
(1) Orbitty carrier board (for Jetson)
(1) Hokuyo 10LX or 30LX LIDAR
(1) Traxxas LiPo or NiMH battery (at least 9V)
(1) FOCbox or VESC 4.12 electronic speed controller
(1) USB hub (at least 6 ports)
(1) short (~1 ft) USB micro cable
(2) spools/strips of 22 AWG wire of different colors (preferably red and black)
(1) USB keyboard and mouse
(1) HDMI display
Optional: (1) HDMI dummy plug and (1) USB Wi-Fi adapter for connecting to the car via VNC

Tools
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
(1) Metric ruler
(1) Needle-nose pliers
(1) Wire strippers
(1) 2mm width or smaller flathead screwdriver
(1) 5/64 inch diameter hex driver key or small Phillips screwdriver (1) Hex socket driver or wrench (to hold standoffs in place)
(1) T3 Torx screwdriver`.

Bill of Materials
------------------------

Insert BOM here.

Preparing and Assembling the Car
---------------------------------

Preparing the Car
----------------------------
Coming Soon: will fill out when the fourth Traxxas car arrives

Obtaining the Power Board
[Instructions on getting the power board from Penn,
and a link to files that you would send to a PCB company like 4PCB or PCBWay. Currently on ​github​]
A note on why we have a power board:​ The power board is used to provide a stable voltage source for the car and its peripherals since the battery voltage drops as the battery runs out. The board does not do any charging of the battery, so you will need a Traxxas EZ-Peak charger to charge it (you can find them on Traxxas' website). At present, there's no way to know the battery's charge level except by measuring it with a multimeter or the BLDC Tool as it runs, but we could think about adding a low voltage LED or seven-segment LCD display (to show the voltage) to the next iteration of the board. The LIPO protection module and green connectors are currently unused and are a legacy from previous F1/10 car iterations which used the Teensy microcontroller as a motor driver.

Installing the Body Standoffs
------------------------------
Begin by installing four 45mm M3 standoffs into the holes of the main car body pictured below. Secure the standoffs to the bottom of the car using 10mm M3 screws, and use either nosepliers or a hex driver to hold the standoff in place while you turn the screw on the other side. Pay attention to where you install the standoffs since there are several mounting holes on the car's base. See the picture below for clarification.

Next, install two threaded 14mm M3 standoffs into the front holes in the car base, using the pliers or hex driver to thread the standoffs into the holes. Don't mount the chassis to the car yet since we still need to mount the Jetson and power board to the chassis.


