# BadgerStick
Our school librarian got some old used BadgerStick boards a few years ago and asked me if there was anything she could do with them as an activity for her kids. Turns out they were a little too fiddly for small kids to enjoy, but I had fun tinkering around enough to get "Hello World" scrolling across its LEDs. Here's the notes I wrote up for her in case anyone else comes across one.  


# What is a BadgerStick?
A BadgerStick is a small Arduino-compatible device that was part of a cool Maker event sponsored by Sparkfun at SXSW in 2015. Kids learned to assemble, solder, and program a badge consisting of the BadgerStick and a LED display that can scroll messages.  

What is an Arduino? According to the folks at https://www.arduino.cc:

>Arduino is an open-source electronics platform based on easy-to-use hardware and software. Arduino boards are able to read inputs - light on a sensor, a finger on a button, or a Twitter message - and turn it into an output - activating a motor, turning on an LED, publishing something online. You can tell your board what to do by sending a set of instructions to the microcontroller on the board. To do so you use the Arduino programming language (based on Wiring), and the Arduino Software (IDE), based on Processing.

# How do I get started using it?
## Connect it to your computer

The BadgerStick connects to your computer like a USB thumb-drive.

To avoid having to disconnect it from the attached LED display, you can use a USB extension cord. The end of the BadgerStick with the 4 shiny strips goes into the thick end of the extension cord. You can then just plug the regular end of the cord into a USB port on the computer. Once it's connected, a red LED should light up on the BadgerStick. This is the power light.

## Install the CodeBender Chrome browser extension

CodeBender is a Chrome browser extension that lets us use our browser to write code and install it on the BadgerStick.

Using Chrome, click on the following google app store link. Then click the ‘Add to Chrome’ button and confirm you want to install it.

https://chrome.google.com/webstore/detail/codebender-app/magknjdfniglanojbpadmpjlglepnlko?hl=en

## Look at some example code
An Arduino program is commonly called a "Sketch".

"Hello World" is a good one to start with. This is a sketch that causes a message to scroll across the LED display attached to the BadgerStick.

When you click the following link, the sketch will open in a CodeBender window. The code is in the main section and below it there are 2 dropdown menus with a green “Run on Arduino” button at the right.

https://codebender.cc/sketch:379543#BadgerHack%20Hello%20World.ino

## Install code onto the BadgerStick
On the first dropdown at the bottom of the CodeBender window, select “BadgerStick” under the “SparkFun Electronics” section.

On the second dropdown, select your USB port. This will be something like `COM3` or `COM4` on a Windows machine, and something like `/dev/cu.usbserial-XYZ123` on a Mac.

Click the green "Run on Arduino" button to install the code to the BadgerStick. You should see a “Working…” message followed by “Upload Successful!” when it is finished. A green LED might flicker on the BadgerStick while the code is being transferred.

The code is now running on the BadgerStick and you should see the "Hello world" message scrolling across the LED display.

## Modify the code!
Click the ‘Edit’ button at the top of the code window. Now you can change the “Hello world” message in the code. Find the following line in the main code window:

`Plex.scrollText("Hello world", 1);`

and modify it to read:

`Plex.scrollText("Hello there", 1);`

You can change the text inside the quotation marks to something else, but if the new message is much longer than the original, you might also have to increase the line that adds the 7 second (7000 millisecond) delay:

`delay(7000)`;

Click the green ‘Run on Arduino’ button again to load the new code. Once the “Upload Successful!” notification pops up, the updated message should start scrolling across the display.

## Disconnect the BadgerStick from the computer

Simply unplug it from the USB port. The red LED power indicator will turn off because there is no power coming from the computer anymore. You can turn it back on using the switch on the attached battery case. The red LED power indicator should turn back on and the code should start running.

# What's next?
## Other BadgerStick examples

Here are some more "scrolling LED" examples that should all be able to run on the BadgerStick and can be installed the same way as the "Hello World" example.

https://codebender.cc/search/find/?query=badgerhack

Here are some examples of using the BadgerStick with some additional sensors and inputs:

__Gaming Add-On Kit (joystick and buttons)__

https://learn.sparkfun.com/tutorials/badgerhack-gaming-add-on-kit

__Sensor Add-On Kit (temperature sensor and soil moisture sensor)__

https://learn.sparkfun.com/tutorials/badgerhack-sensor-add-on-kit

__Synth Add-On Kit (noise-making circuit)__

https://learn.sparkfun.com/tutorials/badgerhack-synth-add-on-kit




## Arduino IDE
We used CodeBender to get started because it is so easy to get up and running. However, the standard way to program an Arduino is by using the Arduino IDE. There are detailed instructions on installing and using it at https://www.arduino.cc/en/Guide/HomePage and https://www.arduino.cc/en/Guide/Environment.

To use it with the BadgerStick, you have to download and install some additional support files. The steps are outlined here:
https://learn.sparkfun.com/tutorials/badgerhack#hack-your-badge.

## Other
The BadgerStick is a simplified Arduino device. It doesn't have as many inputs and outputs as a typical full-sized board. See https://www.arduino.cc/en/Main/Products for the entire range of Arduino products.
