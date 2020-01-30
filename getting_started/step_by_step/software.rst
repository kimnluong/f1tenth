.. _doc_software:

Software
==================
On Your Laptop
----------------
Supported Versions
^^^^^^^^^^^^^^^^^^^^
You will need to install the OS Ubuntu Xenial 16.04.01 and ROS Kinetic. Could other combinations work? Sure. Will we support them? Nope.

Install ROS
^^^^^^^^^^^^^^^^^^^^
Go to ROS.org and follow the instructions there to install the version of ROS referenced above.

Note: you might get the following error message when you execute

.. code-block:: bash

	$ sudo apt-get install ros-kinetic-desktop-full

Building dependency tree
Reading state information... Done
Some packages could not be installed. This may mean that you have requested an impossible situation or if you are using the unstable distribution that some required packages have not yet been created or been moved out of Incoming.
The following information may help to resolve the situation:

The following packages have unmet dependencies:
ros-kinetic-desktop-full : Depends: ros-kinetic-desktop but it is not going to be installed

E: Unable to correct problems, you have held broken packages.
You will find many suggestions online. This one worked for us (I'm installing on a Virtual Machine hosted by a MAC OS).

Specifically, these steps (but it's goot to try the steps in the suggested order):

.. code-block:: bash

	$ sudo apt-get -u dist-upgrade
	$ sudo apt-get -o Debug::pkgProblemResolver=yes dist-upgrade

Then re-run

.. code-block:: bash

	$ sudo apt-get update

and re-try installing ros-kinetic-desktop-full

On Jetson
""""""""""""""
On a high level, these are the things that need to be installed on the Jetson.

Linux GUI
Jetpack 3.2 flash
A re-flash of the Connect Tech Orbitty
ROS Kinetic

Connect terminals to the Jetson (aka the device)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
(These instructions are also in the Jeston’s Quick Start Guide under “Force USB Recovery Mode”. Refer to it to see all the buttons, ports and whatnot.)

Connect a display to the jetson via HDMI port
Connect a USB keyboard
Connect the jetson to your host PC via the USB micro-B plug
Plug to power
The Jetson should power on. If it doesn’t, push the ON button.

.. code-block:: bash

	Login: nvidia
	Password: nvidia


Install Linux
---------------
Run

.. code-block:: bash

	$ cat NVIDIA-INSTALLER/README.txt
	
And run the instructions that are in that file to install Ubuntu Linux. Note that TX1 comes with 14.04 LTS and TX2 comes with 16.04 LTS. There may be an additional step for TX1 if the course is using 16.04 LTS.

Flash the Jetpack
----------------------
NOTE: you will need some 14GB of free space on the host computer for this step.

Now that we have the GUI, we want to flash the Jetson with Nvidia’s Jetpack 3.2.

To do this, we need a host computer that is running Linux 14.04 (it seems 16.04 also works - try it if that’s what you have). The Jetpack is first downloaded onto the host computer and then transferred by micro USB cable over to the Jetson. Follow the instructions here.

What if you don’t have a Linux 14.04 computer laying around? (most of us don’t). See ​Appendix A ​ of this doc for an amazing set of instructions by Klein Yuan which details how to use a virtual machine with a Mac to do the flash. Steps would probably work similarly for a PC that is running Virtual Box.

Re-flash the Orbitty
------------------------
After the Jetson has been flashed with Jetpack, we will actually need to re-flash it with the Connect Tech Orbitty firmware. Otherwise on the TX2 there can be issues with the USB 3.0 not working on the Orbitty carrier board. A great link to instructions is from NVIDIA-Jetson. Note that each time you flash all of the files will essentially be deleted from your Jetson​. So make sure to save any work you may have already done and upload it.

Install ROS
----------------
Lastly, we will want to install ROS Kinetic. Jetson Hacks on Github has scripts to install ROS Kinetic.

Here for TX2: ​ https://github.com/jetsonhacks/installROSTX2​.
And here for TX1: ​https://github.com/jetsonhacks/installROSTX1​.