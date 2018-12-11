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
# Copyright (c) 2014 Adafruit Industries
# Author: Tony DiCola
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.
import time

import Adafruit_GPIO.SPI as SPI
import Adafruit_SSD1306

from PIL import Image


# Raspberry Pi pin configuration:
RST = 24
# Note the following are only used with SPI:
DC = 23
SPI_PORT = 0
SPI_DEVICE = 0

# Beaglebone Black pin configuration:
# RST = 'P9_12'
# Note the following are only used with SPI:
# DC = 'P9_15'
# SPI_PORT = 1
# SPI_DEVICE = 0

# 128x32 display with hardware I2C:
disp = Adafruit_SSD1306.SSD1306_128_32(rst=RST)

# 128x64 display with hardware I2C:
# disp = Adafruit_SSD1306.SSD1306_128_64(rst=RST)

# 128x32 display with hardware SPI:
# disp = Adafruit_SSD1306.SSD1306_128_32(rst=RST, dc=DC, spi=SPI.SpiDev(SPI_PORT, SPI_DEVICE, max_speed_hz=8000000))

# 128x64 display with hardware SPI:
# disp = Adafruit_SSD1306.SSD1306_128_64(rst=RST, dc=DC, spi=SPI.SpiDev(SPI_PORT, SPI_DEVICE, max_speed_hz=8000000))

# Initialize library.
disp.begin()

# Clear display.
disp.clear()
disp.display()

# Load image based on OLED display height.  Note that image is converted to 1 bit color.
if disp.height == 64:
    image = Image.open('happycat_oled_64.ppm').convert('1')
else:
    image = Image.open('happycat_oled_32.ppm').convert('1')

# Alternatively load a different format image, resize it, and convert to 1 bit color.
#image = Image.open('happycat.png').resize((disp.width, disp.height), Image.ANTIALIAS).convert('1')

# Display image.
disp.image(image)
disp.display()
## Testing



