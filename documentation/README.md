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
The connection from the AMG8833 sesor to the Raspberry Pi 3 is very simple and does not require anything ohter then the 2 devices themselves and some wiring. [This post on instructables](https://www.instructables.com/id/Thermal-Camera-AMG833-Raspberry-Pi/) is where I retrieved my wiring diagram and is also where I got the base for my test code later in the build. You can also reference [this diagram](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/Fritzing%20Files/BreadBoard.png) I created in Fritzing.

### PCB / Soldering

Due to only needing 4 wires to connect the AMG8833 sensor to the Raspberry Pi 3 it makes creating the PCB and soldering the header pins onto it very simple. I used Fritzing to create the [diagram](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/Fritzing%20Files/PCB.png) for the PCB.
The rest of the Fritzing files are included [here](https://github.com/kyelehaynes/CENG317HardwareProject/tree/master/Fritzing%20Files) if you would like to use them.

If you do decide to create your own PCB just make sure the traces for the sensor connection and the Raspberry Pi connection are on the correct sides for soldering.
The traces on the sensor connection side need to be on the bottom as you will be soldering the header pins at the bottom. 
The traces for the Raspberry Pi connection will need to be at the top as you will be soldering those header pins on the top. 
Here are the pictures of my PCB all soldered and ready to go; [Soldered PCB Top](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/PCB%20Soldered%20Top.jpg), [Soldered PCB Bottom](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/PCB%20Soldered%20Bottom.jpg)

### Power Up



### Unit Testing



### Production Testing


