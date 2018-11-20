## Kyele Haynes

### Week 12
###### November 20th, 2018
##### Pi Case Due
Today I completed my case drawing in Corel Draw and submitted it to the prototype lab. I used the [Pi2CaseX6.cdr](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/Pi2CaseX6.cdr) from dropoffs as a starting point for my custom case. File: [PiCase_AMG8833_Drawing.cdr](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/PiCase_AMG8833_Drawing.cdr). I got help from Kelly in the prototype lab on how to use the Corel Draw software and modify the file to my needs. I had to raise the height of the whole case by 0.5" and add a cutout at the top for my sensor. 

##### Screenshot of Corel Draw Drawing
![Screenshot of Corel Draw Drawing](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/Case%20Drawing.PNG)

This week the case was supposed to be cut and assembled around my pi. Unfortunately I did not get to that point as I started on my Corel Draw file late due to a lack of knowledge of the program. I missed the deadline of having the case cut today by an hour or 2 so I will have to pick it up later this week and make another blog entry when I have my Pi enclosed in it. Thus, I am currently a little bit behind in regards to my [project schedule](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/CENG317ProjectSchedule.mpp). As per my [project budget](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/Project%20Budget.xlsx) this week had no effect because the machine and acrylic used to create the case are provided to me by the college and the Corel Draw software is available on the lab computers.

### Week 11
###### November 13th, 2018
##### PCB Power Up and Test Code
Today the first thing I did was solder 1 more pin on my Raspberry Pi header on my PCB. This was only done for stabilility as the header was moving around a bit more than I liked. Next I powered up my Pi with the PCB connected and ran i2cdetect one more time to make sure it was still communicating with my AMG8833 sensor which it was. Next I found [this page on Adafruit](https://learn.adafruit.com/adafruit-amg8833-8x8-thermal-camera-sensor/python-circuitpython) which demonstrates some test code to communicate with the AMG8833 and how to run it. This is where I started to have some issues as my Raspberry Pi would not connect to the internet for me to be able to download the repositories/dependancies I needed. It took me ~15 minutes to solve the issue which had to do with the Internet sharing settings between network adapters in Windows being setup wrong. Once I had the dependancies downloaded I was able to run the code from the website mentioned above. I then added a timestamp to each sensing loop of the IR sensor and changed the delay from 1 to 5 seconds for readablility. As you can see in the screenshot below there are 2 loops that ran showing the 8x8 grid of the sensor 5 seconds apart. The first one is with nothing covering the sensor and the second is with my finger covering it, explaining why the read temperatures are much higher.

##### Screenshot of Running Code
![Screenshot of Running Code](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/AMG8833%20Code%20Test.png)

As per my [project budget](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/Project%20Budget.xlsx), this weeks accomplishments had no effect on it because I was mainly working on software. As per my [schedule](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/CENG317ProjectSchedule.mpp), I am still on track.

### Week 10
###### November 6th, 2018
##### PCB Soldering 
Yesterday, November 5th, I went to the prototype lab to pick up my PCB and verify that it will work. Today I soldered the stackable header pins for the sensor and Pi. I also soldered the via holes.

##### Soldered PCB Top
![Soldered PCB Top](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/PCB%20Soldered%20Top.jpg)

##### Soldered PCB Bottom
![Soldered PCB Bottom](https://raw.githubusercontent.com/kyelehaynes/CENG317HardwareProject/master/documentation/PCB%20Soldered%20Bottom.jpg)

The first issue I ran into today was that I did not have any [stackable header pins](https://www.google.ca/search?q=stackable+header+pins&safe=strict&rlz=1C1GGRV_enCA751CA751&source=lnms&tbm=isch&sa=X&ved=0ahUKEwj88_K178DeAhVtUd8KHaGZCJcQ_AUIDigB&biw=1920&bih=930). Luckily there were available ones in the prototype lab for the Pi and there was one I was able to modify for my AMG8833 sensor. As per soldering it went pretty well as I have had experienece in the past. I did have some trouble with the solder balling up a lot at the beginning and was not sticking. After playing with the heat settings on the soldering iron and adjusting my technique slightly I was able to get it to stick fairly well. I checked my solders under the microscope and all seemed well. Once I finished soldering the Pi header onto the board I plugged it all toether and connected to my Pi through RDP and ran sudo i2cdetect -y 1 again to verify that the Pi was detecting the AMG8833 on the PCB and it was. Since I fully completed the soldering today I am still on track as per my [project schedule](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/CENG317ProjectSchedule.mpp). Due to getting my stackable header pins from the prototype lab today I am still on track as per my [project budget](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/Project%20Budget.xlsx)


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
According to my [schedule](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/CENG317ProjectSchedule.mpp) I am on track so far, Next I need to begin interacting with and recieving data from my sensor with the Raspbian OS on the Raspberry Pi to remain on schedule. As per the [project budget](https://github.com/kyelehaynes/CENG317HardwareProject/blob/master/documentation/Project%20Budget.xlsx) I had to purchase an SD card last week for the Raspbian OS which I had overlooked originally. This adds ~$12 to the total amount spent on the project which is not an issue. Other than that I have not had any other issues.


### Week 8
###### October 23rd, 2018
##### During Class
I Repurchased my parts kit this week as I had misplaced my previous one, I also purchased a 32GB micro SD card. In class I began wiring my AMG8833 sensor to my Raspberry Pi 3, making use of a breadboard. Once I began wiring I soon realized I do not have the special wires to plug into the header pins on the Raspberry Pi and to the breadboard. To get around this I broke off single header pins, plugged them into the breadboard. I then used aligator clips on the individual header pins and on the header pins on the Raspberry Pi to make my connections, using small pieces on paper to prevent shorts on the Pi. I will eventually clean up my wiring but as of right now it does not matter. During class I also copied the required NOOBs files to the root of my 32GB SD card. I was not able to begin setting up the image on my Pi as there was a shortage of display adapters, something out of my hands. Thus, later today I will set up the image at home where I have the proper equipment and make another blog post. During this time I also found a [helpful post on instructables](https://www.instructables.com/id/Thermal-Camera-AMG833-Raspberry-Pi/) which will help me when setting up the image on my Pi, this link is also where I found my wiring diagram.

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
