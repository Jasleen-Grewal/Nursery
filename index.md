OLED MONOCHROME GRAPHIC DISPLAY
===============================

In my project I will work to make my OLED display working with raspberry pi 3. Basically my display will show the current readings of temperature, humidity and moisture level in soil. I am storing these values in my database and I will retrive these values using python code.
### November 27, 2018
Here is the link to my powerpoint presentation for my hardware project: [link](https://github.com/Jasleen-Grewal/Nursery/blob/master/JasleenKaur.pptx)

### November 23, 2018
 After redesigning my PCB I figured that I have to change the height, length and width to make it fit in raspberry pi case. I takes me around 3-4 hours to design case for my display because I have to change dimensions keeping even minor measurements in mind. But finally I made my case with the help of Kelly:
![displaycase1](https://user-images.githubusercontent.com/43180933/48969782-86964b00-efd1-11e8-8684-c71ecbbe5580.jpeg)
![displaycase2](https://user-images.githubusercontent.com/43180933/48969788-944bd080-efd1-11e8-9d62-35fdec00699b.jpeg)

### Corel Draw of my file could be found [here](https://github.com/Jasleen-Grewal/Nursery/blob/master/jasleenCase.cdr)
### This is how my corel diagram looks like:
![case](https://user-images.githubusercontent.com/43180933/48984224-37cadd00-f0c7-11e8-8378-0a1d9abfb3ef.PNG)



### November 20, 2018
 In this week I have to design case for my OLED display. As size of my PCB is quite large therefore it becomes hard for me to disgn the case of for my display. Kelly suggests me to redeign a smaller PCB so that it fits in the raspberry pi case and we need to change its height.

Working of OLED Display:
=======================
I installed library for monochrome OLED display from adafruit and make my OLED display working using python:

![sensor](https://user-images.githubusercontent.com/43180933/48816773-7f411a00-ed11-11e8-8dbb-e1c458ded3bb.jpg)

Soldering:
===========
Using my fritzing diagram I made design of my PCB and send to prototype lab to design the PCB for my OLED display. Next week I did the soldering of my PCB to make my OLED display working without use of breadboard and jumper wires.

![pcb](https://user-images.githubusercontent.com/43180933/48099161-b5987880-e1ec-11e8-977b-598e06d49b42.jpg)

PCB Design:
===========
Here is the PCB design of my OLED display:

![sensor_pcb](https://user-images.githubusercontent.com/43180933/48093062-4dda3180-e1dc-11e8-9711-40fb660170dd.jpg)

Fritzing:
=========

After displaying the address of my OLED display, I designed the fritzing diagram of all the connections that I made on breadboard to diplay address to make the PCB design for the circuit.

![untitled sketch_bb](https://user-images.githubusercontent.com/43180933/47751096-43adb580-dc67-11e8-9d7b-385b1a163744.png)

Breadboarding:
==============
Earlier I was unable to get the address of OLED display because by default the chip in the module is working on SPI. Therefore, I have to change the resistor position on the module to make it work on I2C circuit.

After taking help from kelly I got the address of my OLED display.
![whatsapp image 2018-10-25 at 9 28 35 pm 1](https://user-images.githubusercontent.com/43180933/47597854-9df60000-d961-11e8-80e7-67cb6ff353da.jpeg)
Here is the breadboard circuit design of my OLED display:
![whatsapp image 2018-10-25 at 9 28 35 pm](https://user-images.githubusercontent.com/43180933/47597862-b239fd00-d961-11e8-960c-9d9d833bcc54.jpeg)

### Resolution: Kristian refered me to kelly/Vlad for the issue in the breadboarding of my sensor.
Initial Breadboarding: I designed the circuit for my OLED display but unable to get the address of my display:

![jasleen](https://user-images.githubusercontent.com/43180933/47393750-5b78bd00-d6ee-11e8-85c5-c7e02b80b463.jpg)

# Invoice
## Monochrome OLED display
![inkedcapture_li](https://user-images.githubusercontent.com/43180933/46378961-4ec2f500-c66b-11e8-9ca0-0cf130a3aa82.jpg)

## Raspberry pi
![capture](https://user-images.githubusercontent.com/43180933/46379019-83cf4780-c66b-11e8-83dd-57b97c93632f.PNG)
