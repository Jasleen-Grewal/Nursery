Build Instructions for 1305 Monochrome OLED Display:
====================================================
## Introduction:
The project aims to diplay the current temperature, humidity at a particular place. My diplay, Monochrome OLED Display 1305 is quite readable due to its high contrast. Moreover, this display is made of 128x32 individual blue OLED pixels, each one is turned on or off by the controller chip. Also, this display makes its own light therefore no background light is required. This results in reduction of power required to run the OLED and is why the display has such high contrast. I really like this graphic display for its crispness!<br>

![proposalforhardware](https://user-images.githubusercontent.com/43180933/49705814-3d5c1300-fbef-11e8-890e-07a907621242.PNG)

## Budget
The stuff required to make my OLED working is Raspberry pi kit, which I brought from amazon. Another thing that was required was monochrome OLED Display, which I purchased from Adafruit.<br>

![budgetforhardware](https://user-images.githubusercontent.com/43180933/49705945-59ac7f80-fbf0-11e8-821e-965189972120.PNG)

## Time Commitment
Overall project is planned to complete in 15 weeks but if someone already purchased the raspberry pi and OLED display, I can say that it will just take around 2-3 weeks to rebuild the whole project except the time required to design the PCB for the display.<br>

![schedule](https://user-images.githubusercontent.com/43180933/49832270-27bc2a00-fd64-11e8-983a-34ea43f0a31d.PNG)

## System Diagram
![systemdiagram](https://user-images.githubusercontent.com/43180933/49834777-4114a480-fd6b-11e8-815e-42ef9fa89a5a.PNG)

## Mechanical Assembly
![pinlayout](https://user-images.githubusercontent.com/43180933/49834382-3c032580-fd6a-11e8-9d43-70839d13152f.PNG)

## PCB Design:
For my PCB design I made my fritzing diagram and sent gerber files to humber prototype lab to get my PCB design
Link to my fritzing diagram is [here](https://github.com/Jasleen-Grewal/Nursery/blob/master/sensor.fzz)

![pcbdesign](https://user-images.githubusercontent.com/43180933/49835658-ef214e00-fd6d-11e8-8c91-eb5a7f47f169.PNG)

## Setting up Raspberry Pi
After receiving the order, the first step is installing Raspian on Raspberry Pi.These are the steps for installation as given below:-<br>
**Step 1: Download Raspbian**<br>
It can easily take more than half an hour to download the software.Download Noobs from https://www.raspberrypi.org/downloads/<br>

**Step 2: Unzip  the file**<br>
The Raspbian disc image is compressed, so you’ll need to unzip it. The file uses the ZIP64 format, so depending on how current your built-in utilities are, you need to use certain programs to unzip it.<br>

**Step 3: Write the disc image to your microSd card**<br>
Select the drive of your SD card in the ‘Device’ dropdown.

**Step 4: Put the microSD card in your Pi and boot up**<br>
Select ‘Write’ and wait for the process to finish which may take around 20 minutes to complete.

## Writing the Script for monochrome OLED Display
**Here is a link to my python [code](https://github.com/adafruit/Adafruit_Python_SSD1306)**
![pythoncode](https://user-images.githubusercontent.com/43180933/49834174-bf704700-fd69-11e8-9fed-bae6b7422870.PNG)
## Testing
When I run my pyhton code I got my display working.<br>

![testing](https://user-images.githubusercontent.com/43180933/49834540-a2884380-fd6a-11e8-89b5-312743589c27.PNG)

## Enclosure:
To provide a case for my display you can use my coreldraw file to get similar enclosure as below:<br>

![enclosure](https://user-images.githubusercontent.com/43180933/49835880-a1f1ac00-fd6e-11e8-872a-5ee516fe5049.PNG)


