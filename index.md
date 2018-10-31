## Kyele Haynes


### Week 9
###### October 30th, 2018
##### Fritzing + PCB 
Today in class I designed my PCB using Fritzing. I did not have many issues with this as I only require 4 connections on my PCB. I have used Fritzing in the past for a project in highschool, thus I was already familiar with the software but needed a refresher as in the past I have only manually etched single sided PCB's. Here are the exported PNG's of the Fritzing diagrams:

##### Fritzing Breadboard
![Fritzing Breadboard](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/Fritzing%20Files/BreadBoard.png)

##### Fritzing PCB
![Fritzing PCB](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/Fritzing%20Files/PCB.png)

Once I finished the design of my PCB and made small modifications to fit my needs I sent an email to the Prototype lab and attached the Extended Gerber files in a zip format exported from Fritzing. Below is a screenshot of my sent email:

##### Email to Prototype lab
![Email to Prototype Lab](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Email%20to%20Prototype%20Lab.PNG)

##### Progress/Status Update
According to my schedule I am on track so far, Next I need to begin interacting with and recieving data from my sensor with the Raspbian OS on the Raspberry Pi to remain on schedule. As per the budget I had to purchase an SD card last week for the Raspbian OS which I had overlooked originally. This adds ~$12 to the total amount spent on the project which is not an issue. Other than that I have not had any other issues.


### Week 8
###### October 23rd, 2018
##### During Class
I Repurchased my parts kit this week as I had misplaced my previous one, I also purchased a 32GB micro SD card. In class I began wiring my AMG8833 sensor to my Raspberry Pi 3, making use of a breadboard. Once I began wiring I soon realized I do not have the special wires to plug into the header pins on the Raspberry Pi and to the breadboard. To get around this I broke off single header pins, plugged them into the breadboard. I then used aligator clips on the individual header pins and on the header pins on the Raspberry Pi to make my connections, using small pieces on paper to prevent shorts on the Pi. I will eventually clean up my wiring but as of right now it does not matter. During class I also copied the required NOOBs files to the root of my 32GB SD card. I was not able to begin setting up the image on my Pi as there was a shortage of display adapters, something out of my hands. Thus, later today I will set up the image at home where I have the proper equipment and make another blog post. During this time I also found a helpful post on instructables which will help me when setting up the image on my Pi, this link is also where I found my wiring diagram. https://www.instructables.com/id/Thermal-Camera-AMG833-Raspberry-Pi/

##### Pi to Sensor Wiring
![Pi to Sensor Test Wiring](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Pi%20to%20Sensor%20Wiring.jpg)

##### At Home
Had no issues setting up RDP connection to the pi (using xrdp) and ssh connection. Also enabled the I2C and VNC services. I ran sudo i2cdetect -y 1 to check if my Pi is detecting my sensor (0x69) and it did. (screenshot shown below)

##### I2C Detect Command Shown Running on my Pi
![I2C Detect](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/I2CDetect.PNG)

### Week 7
###### October 16th, 2018

##### Parts Ready in Lab
![Ordered Parts](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Ordered%20Parts.jpg)

##### Me Soldering the Header Pins on the Sensor
![Soldering the Sensor](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/soldering.jpg)
Finished soldering the header pins onto my AMG8833 sensor

### Week 6
###### October 9th, 2018

No class due to Thanksgiving + Study days
During this week my parts that were ordered last week had been delivered

### Week 5
###### October 2nd, 2018

##### Parts Receipt
![Parts Receipt](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Parts%20Receipt.png)

Ordered on October 2nd, 2018

### Week 4
###### September 18th, 2018

Submitted project budget spreadsheet

[Project Budget](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/Project%20Budget.xlsx)

### Week 3
###### September 11th, 2018

Submitted Project Plan (Gantt Chart)

[Project Plan](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/CENG317ProjectSchedule.mpp)

### Week 2
###### September 4th, 2018

Submitted Project Proposal

[Project Proposal](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/ProposalContentStudentNameRev02.xlsx)

### Week 1
###### September 25th, 2018

Started the project

Created the repository
