.. _doc_hardware:


Hardware
==================

.. image:: img/f10cover.png

.. centered::
	`Download PDF here <http://f1tenth.org/build/BuildV2.pdf>`_

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

[INSERT LINK TO BOM HERE]

Preparing and Assembling the Car
---------------------------------

Preparing the Car
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Coming Soon: will fill out when the fourth Traxxas car arrives

Obtaining the Power Board
[Instructions on getting the power board from Penn,
and a link to files that you would send to a PCB company like 4PCB or PCBWay. Currently on ​github​]
A note on why we have a power board:​ The power board is used to provide a stable voltage source for the car and its peripherals since the battery voltage drops as the battery runs out. The board does not do any charging of the battery, so you will need a Traxxas EZ-Peak charger to charge it (you can find them on Traxxas' website). At present, there's no way to know the battery's charge level except by measuring it with a multimeter or the BLDC Tool as it runs, but we could think about adding a low voltage LED or seven-segment LCD display (to show the voltage) to the next iteration of the board. The LIPO protection module and green connectors are currently unused and are a legacy from previous F1/10 car iterations which used the Teensy microcontroller as a motor driver.

Installing the Body Standoffs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Begin by installing four 45mm M3 standoffs into the holes of the main car body pictured below. Secure the standoffs to the bottom of the car using 10mm M3 screws, and use either nosepliers or a hex driver to hold the standoff in place while you turn the screw on the other side. Pay attention to where you install the standoffs since there are several mounting holes on the car's base. See the picture below for clarification.

Next, install two threaded 14mm M3 standoffs into the front holes in the car base, using the pliers or hex driver to thread the standoffs into the holes. Don't mount the chassis to the car yet since we still need to mount the Jetson and power board to the chassis.

Mounting the FOCbox to the Chassis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Feed the three motor wires for the FOCbox through the rectangular slot in the chassis as shown below.



Alternate method of securing the FOCbox if screws don’t fit​ : Some FOCboxes (the more recently-made ones) have smaller screw holes that won’t fit M3-size screws. If this is the case for your FOCbox, you can use a few pieces of double-sided tape to secure the FOCbox instead.



Installing the Chassis Standoffs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Mount eight 35mm M3 standoffs to the ​ glossy side​ of the black laser-cut chassis in the positions shown below. Thread 10mm M3 screws through the drill holes and screw them into the standoffs to secure them. (​ Important​ : If you do not mount the standoffs to the glossy side, the power board won't fit since the screw holes will be misaligned.)

Note there are several drill holes in the chassis, so make sure you’re using the right ones. In the image below, the 4 screws on the left(which is the back of the car) will eventually hold the power board, so that’s a good way to see if they’re properly placed. The 4 screws on the right (2 on each side of the oval cutout) will eventually hold the Orbitty carrier attached to the Jetson.



Mount two more (19mm M3) standoffs to the front part of the chassis for the LIDAR, and secure with 10mm screws. The top part of the chassis should look like the picture below.



Detaching the Jetson from the Development Board
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you purchase a Jetson, it is attached to a development board. In order to use it on the car, you will need to unscrew the Jetson and its Wi-Fi antenna from the development board.

Before you remove the antenna, you will need to remove the bottom plate from the development board. Remove the four screws marked below and lift the development board away from the plate.



Next, remove the Wi-Fi antenna by unscrewing the two screws marked below. Keep the screws in a safe place, as you’ll use them in a bit to attach the antennas to standoffs.



Remove the two brass-colored nuts holding the antennas to the L-shaped bracket, and then remove the two antennas from the bracket. It helps to use two pairs of pliers: one to hold the rear nuts in place and another to unscrew the nuts on the end with the antenna connectors.



Using a Phillips screwdriver, thread the two screws you saved earlier completely into the bracket as pictured below. Attach two standoffs to the opposite ends of the screws and hand-tighten them until they won’t turn anymore. Use the pliers to tighten the standoffs more while you hold the head of the screw in place using the screwdriver. Once you’ve done these steps, place the antennas and washers back into the bracket, and tighten the brass nuts onto the threaded connectors again.



Unplug the Jetson’s fan and remove the Jetson from the development board by using a T3 Torx screwdriver to unscrew the Jetson (the large silver heat sink), and then pull up gently to detach it from the development board. Keep the Jetson in a safe place while you attach the antennas to the power board.



Mounting the Wi-Fi Antennas to the Power Board
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Attach the two standoffs for the Wi-Fi antenna bracket to the power board, making sure the antennas, when installed and extended, lie ​ over ​ the board and now away from it. Install the two black antennas onto the threaded connectors if they aren’t already on.



Attach the two wires for the Jetson Wi-Fi antenna to the two gold-colored connectors near the fan connector on the heat sink (the order of the wires doesn’t matter). This can be a little tricky, so you might want to use a flathead screwdriver to ensure the connections are tight. ​ Don’t press too hard​ , however as you can easily damage the connectors if you use excessive force!



Mounting the Power Board to the Chassis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Screw the power board onto its chassis standoffs using 10mm M3 screws. The screw positions are indicated with arrows below.



Attaching the Orbitty to the Jetson
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Attach the Orbitty to the Jetson by connecting the two long black ports and connect the Jetson’s fan to the Orbitty’s fan connector as shown in the pictures below.



Connecting the Jetson and Power Board
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cut two 8-inch pieces of wire of different colors (preferably red and black), and strip both ends to a short length (1/8 inch). Locate the green terminal block on the Jetson and attach one end of one wire to the + ​ Vin​ terminal, and the other end to one of the green 1 ​ 2V​ terminals on the power board. (Any of the 12 volt terminals are acceptable. To attach, insert the stripped end into the terminal and screw the little screw tight with a small flathead screwdriver.) Attach the other stripped wire to the G ​ ND​ terminal on the Jetson and to the G ​ ND​ terminal on the corresponding terminal block on the power board.



Mounting the Jetson to the Chassis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Your kit comes with four white plastic standoffs; place these between the Jetson PCB and heatsink (see picture) ​ before ​ threading the screws through. Otherwise, you risk bending the Orbitty while screwing it in. Use 20mm screws to secure the Jetson to its chassis standoffs.



Ensure that when you mount the Jetson that the wires for neither the Wi-Fi antenna nor the Jetson's power connections get pinched. It might help to tuck both sets of wires underneath the power board. (Don't tuck them underneath the Jetson because they might restrict airflow or obstruct the fan's blades.) Your configuration should now look something like this:



Mounting the Chassis to the Car Underbody
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Place the chassis onto the five standoffs on the car base and align the chassis’ drill holes with the car’s base standoffs you attached earlier as shown below. Use six 10mm M3 screws to secure the chassis to the standoffs.



Mounting the LIDAR
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The LIDAR should have two cords: one for power and another for either Ethernet or USB. Cut the end of the power cord, leaving 1-2 feet of cable. Strip the end, cut away all wires except for the blue and brown ones, and strip those two wires to 1/8 inch as shown below.



Attach the LIDAR to the tree-shaped base using two (10LX) or four (30LX) screws, such that the wires protruding from the LIDAR go towards the back of the car. (For the 30LX, the two LEDs at the top of the LIDAR should face the front of the car.) Then mount the C-shaped brackets to the black tree-shaped base as shown in the pictures below. ​ Note: if the black mount does not fit in the holes of the C brackets, sand the inserts until they do.



Mount the LIDAR to the car by fitting the two thick protruding parts of the mounting brackets into the holes. The open part of the "C" in the brackets should face forward as shown below.



If you completed the previous steps correctly, two of the holes on the narrow end of the LIDAR base should match up with the two 19mm standoffs you mounted earlier. Wind the power and USB cords of the LIDAR around its base so that there is just enough available to plug into the power board and Jetson, with a little bit of slack so that it is not too tight. Tuck both cords under the LIDAR mounting plate between the two silverstandoffs, and secure the LIDAR base to the standoffs on the chassis using two 10mm M3 screws.



Mounting the USB Hubs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Attack two pieces of double-sided tape to a USB hub. Place the hub onto the empty space of the chassis directly below the Jetson and to the right of the power board as shown. If your hub has power buttons, make sure all of them are turned on.



If you need more USB ports (required if your LiDAR uses USB), you can stack a second hub onto the top of the first. Again, use double-sided tape to secure the second hub and make sure all power buttons are on.

Plug the first USB hub into the Orbitty board. If you’re using a second hub, use the white micro USB adapter that comes with the Jetson to plug in the second hub.



Connecting the LIDAR
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Attach the LIDAR's power cable to a free 12V terminal block on the power board. The brown wire should go to the 12V terminal, and the blue wire should go to the corresponding GND terminal. The side of the LIDAR has a pinout as well if you forget.



If the LIDAR has an Ethernet cable, attach it to the Ethernet port on the Jetson. If it has a USB cable, plug it into the USB hub. Route any excess cables behind the USB hubs as shown.



Connecting the FOCbox
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Pass the 3 round FOCbox wires through the rectangular slot in the plastic chassis, then connect the 3 circular bullet connectors to the three motor wires. (The order in which you connect the wires kinda doesn’t matter (electrically speaking). If you run the car and it goes backwards when it should go forwards, you can swap any two of the three wires.) Connect the 3-wire servo ribbon cable as well, making sure the colors match up.



If your micro USB cable is thin enough, thread it through the rectangular wire slot and around the FOCbox to the USB connector as shown below, or route it around the rear end of the chassis if it isn’t. Plug the cable into the FOCbox’s USB connector and into a free port on your USB hub. Tie the USB cable up using a cable tie, and tuck all of the wires underneath the chassis. You can also use this time to plug in the LIDAR (if it is USB), the external Wi-FI adapter, and the receiver for the F710 gamepad.




Connecting the Car to the Battery
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Connect the battery to the FOCbox using the battery connector. ​Make sure that red is aligned with red and black is aligned with black - otherwise things will get hot and dicey. ​Then connect the FOCbox to the power board using the white port shown in the picture below.



At this point, your car should be assembled, the Jetson lights should flash when you flip the power switch, and the car is ready to run!

Note: At present, there's no way to know the battery's charge level except by measuring it with a multimeter as it runs. You might consider adding a low voltage LED or seven-segment LCD display (to show the voltage).

Tuning the FOCbox’s PID Gains
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In this section we use the words FOCbox and VESC interchangeably.

Important Safety Tips
Make sure you hold on to the car while testing the motor to prevent it from flying off the stand.
Make sure there are no objects (or people) in the vicinity of the wheels while testing.
It’s a good idea to use a fully-charged LiPO battery instead of a power supply to ensure the motor has enough current to spin up.
Put your car on an elevated stand so that its wheels can turn without it going anywhere. If you don’t have an RC car stand, you can use the box that came with your Jetson.

Connect the host laptop to the FOCbox using a USB cable.

Download bldc tool from JetsonHacks, following his instructions for installation.

Open BLDC Tool and click the “Connect” button at the top right of the window to connect to the VESC.

If you get the error “Device not found”, try running the command ​lsusb​ in a terminal. You should see an entry for “STMicroelectronics STMF407” or something similar. If you don’t, try unplugging and plugging in the USB cable on both ends. If the problem doesn’t go away, try rebooting the Jetson.


If you are using a VESC 4.12 (including a FOCbox), ensure the firmware version is 2.18.


Disable keyboard control by clicking the “KB Ctrl” button at the lower right. This will prevent your keyboard’s arrow keys from controlling the motor and is important to prevent damage to the car from it moving unexpectedly.



Start plotting the realtime RPM data by clicking the “Realtime Data” tab, and checking the “Activate sampling” checkbox at the bottom left of the window. Click the “RPM” tab above the graph.

We will keep referring to this plot of the motor’s RPM as we tune the PID gains. Out goal is to get the motor to spin up as quickly as possible when we set it to a certain RPM. We also don’t want the motor to cog (not spin) or overshoot the target speed if possible.


Test the motor first (without PID speed control) by setting the “Duty Cycle” to 0.20. This will spin the motor up to approximately 16,000 - 17,000 RPM. Let this run for a few seconds, and then press the “Release Motor” button at the bottom right to stop it.
Observe the RPM graph. If the motor is spinning backwards (the RPM is negative), try reversing two of the connections from the VESC to the motor. (It doesn’t matter which wires you reverse.)
If the wheels don’t spin and the motor makes no noise, check to make sure all connections to the motor are tight.
If the wheels don’t spin and the motor does, ensure the motor’s gear is attached correctly to the gearbox at the back of the car. Spin both front wheels with your hand to verify that the gear is making good contact. You should feel some resistance when turning the wheels.
If the motor doesn’t spin and makes a humming or hissing sound, you might need to replace the motor. If this doesn’t work, try replacing the VESC.


Click the “Motor Configuration” tab at the top and the “Advanced” tab on the left. Set Ki and Kd to 0.00000, and set Kp to 0.00001. Click the “Write Configuration” button at the bottom, go back to the data plotting tab and run the car at 3000 RPM.
You will notice that the car won’t even make it close, as it only goes up to around 1200 RPM. (High steady-state error.)
Try turning Kp up to 0.00002, 0.00004, and 0.00008. (Don’t forget to write the configuration each time.) The motor will start to cog out at higher Kp values.


Set Kp back to 0.00002, and set Ki to 0.00002, and run the car at 3000 RPM again. Notice how the car slowly reaches the 3000 RPM target. (This is because adding Ki helps to eliminate steady-state error.)
Keep increasing Ki; set it to 0.00005 and then double that value a few times until the car is able to reach 3000 RPM without overshooting or cogging out.
Now, try increasing the speed to 6000 RPM.
The motor might cog out and overshoot. If it does, try halving Kp.
Increase the speed to 10,000 RPM and then 20,000 RPM. ​Make sure you hold the car!
If the motor cogs out and overshoots, halve Kp until it doesn’t.
It may also help to halve Ki if halving Kp doesn’t work.
If done correctly, the motor should not overshoot to more than 2 times the set RPM. (That is, if the RPM is set to 15,000, its peak value should not exceed 30,000.)

LiPo (Lithium Polymer) Battery Safety
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
LiPO batteries allow your car to run for a long time, but they are not something to play with or joke about. They store a large amount of energy in a small space and can damage your car and cause a fire if used improperly. With this in mind, here are some safety tips for using them with the car.

When charging batteries, always monitor them and place them in a fireproof bag on a non-flammable surface clear of any other objects.
Do not leave a LIPO battery connected to the car when you’re not using it. The battery will discharge and its voltage will drop to a level too low to charge it safely again.
Unplug the battery from the car immediately if you notice any popping sounds, bloating of the battery, burning smell, or smoke.
Never short the battery leads.
Do not plug the battery in backwards. This will damage the VESC and power board (and likely the Jetson as well) and could cause a short circuit.
See ​this video​ and ​this video​ for examples of what might happen if you don’t take care of your batteries. Be safe and don’t let these happen to you!