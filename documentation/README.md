# CENG317HardwareProject
## Build Instructions

### Intro

This README file will outline the build instructions for the project displayed in this repository. First off, here is the [System Diagram](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/System%20Diagram.png) for the project.

As you can see the project will use the AMG8833 IR Sensor take the thermal data emitted by people in a room. It will then use the Raspberry Pi 3 the sensor is connected to to upload said data to a database which can then be displayed in a web or mobile application.

What is the point of this device? It is meant to be placed in a meeting room, lab, study room etc. so other people in the building who may be interested in making use of the room are able to check if it is free or not.

### Bill of Materials/Budget

Here is [a list](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Final%20Budget.PNG) of all the materials purchased and their prices.

In total this project would cost $290.49. For anyone else wanting to reproduce the project it could probably be done a but cheaper as the entire parts kit is not needed. The only things needed from it are a breadboard, some wiring to be used on the breadboard and wirecutters. The only other thing you will need is access to a soldering gun and solder.

### Time Commitment



### Mechanical Assembly

Here is my [Pi to Sensor test wiring](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Pi%20to%20Sensor%20Wiring.jpg)

The connection from the AMG8833 sesor to the Raspberry Pi 3 is very simple and does not require anything other then the 2 devices themselves and some wiring. [This post on instructables](https://www.instructables.com/id/Thermal-Camera-AMG833-Raspberry-Pi/) is where I retrieved my wiring diagram. You can also reference [this diagram](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/Fritzing%20Files/BreadBoard.png) I created in Fritzing.

### PCB / Soldering

Due to only needing 4 wires to connect the AMG8833 sensor to the Raspberry Pi 3 it makes creating the PCB and soldering the header pins onto it very simple. I used Fritzing to create the [diagram](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/Fritzing%20Files/PCB.png) for the PCB.
The rest of the Fritzing files are included [here](https://github.com/kyelehaynes/CENG317HardwareProject/tree/master/Fritzing%20Files) if you would like to use them.

If you do decide to create your own PCB just make sure the traces for the sensor connection and the Raspberry Pi connection are on the correct sides for soldering.

The traces on the sensor connection side need to be on the bottom as you will be soldering the header pins at the bottom. 

The traces for the Raspberry Pi connection will need to be at the top as you will be soldering those header pins on the top. 
Here are the pictures of my PCB all soldered and ready to go: [Soldered PCB Top](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/PCB%20Soldered%20Top.jpg), [Soldered PCB Bottom](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/PCB%20Soldered%20Bottom.jpg)

### Power Up

First of all, copy the [NOOBS](https://www.raspberrypi.org/downloads/noobs/) files onto the root directory of your SD card and insert it into the Pi. The first time powering up the pi use and HDMI cable to connect to a monitor, an ethernet cable for internet access (could use wifi as well) and a keyboard and mouse to setup the Pi. On the NOOBS menu that will come up choose Raspbian and install it. Once Rasbian is installed and you are greeted with the homescreen. Next enable the I2C and VNC services under the menu in the top left corner. Also [install xrdp](https://www.maketecheasier.com/enabling-remote-desktop-access-on-raspberry-pi/) to allow you to connect to the pi via rdp. Once installed, get the ip address of the pi by using ifconfig on the terminal and write it down. You can now disconnect the pi from the monitor, keyboard and mouse. Then connect it to your computer directly using the ethernet cable and then use RDP on your computer to connect to the ip address you get from using ifconfig on the pi. Next, with the sensor connected to the pi, run the [I2C detect](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/I2CDetect.PNG) command on the terminal and if you get the same output (showing 0x69) you have successfully connected the AMG8833 to the Raspberry Pi.

### Unit and Production Testing

Now that the sensor and Pi are setup and can communicate the last few things we have to do are run some test code and create a case to enclose our device. [This page on Adafruit](https://learn.adafruit.com/adafruit-amg8833-8x8-thermal-camera-sensor/python-circuitpython) demonstrates some test code for the AMG8833 sensor in python and explains how to run it. I made a couple modifications to the code for this project for readability purposes and added a timestamp, [here](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/AMG8833%20Code%20Test.png)
 is my code and the output. The output is displayed in 8x8 blocks as that is how the AMG8833 reads data. The first output block is with the sensor sitting on a desk under regular lights and the second block is with my finger over the sensor. As you can see the temperatures go higher with my finger over the sensor as it is sensing my body heat.

The last thing we need is the case. I created mine using Corel Draw and a laser cutter in the prototype lab at humber. [Here](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/PiCase_AMG8833_DrawingV2.cdr) is the CorelDraw file. There is not much to explain here as I would need to go into detail on how to use the software, go ahead and use the file if you would like, or reference it to create your own.
 
