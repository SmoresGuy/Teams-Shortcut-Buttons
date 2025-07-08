# Introduction on my changes

I took the work done by @TellinStories and wanted to make work with Google Meet as that my standard platform at work, but I still wanted to support the Teams on a single box, however that will have to wait. For now, my version introduces a Mac verion of the codes. Each file is named as such.  

## Original content from [Team-Shortcut-Buttons](https://github.com/TellinStories/Teams-Shortcut-Buttons) with _modifications highlighted with italics_

I spend a lot of my work day in _Google and_ Teams  meetings and frequently need to mute / unmute my microphone, turn my camera on and off, or raise or lower my hand.  
If using my mouse I invariably can’t find the right icon to click fast enough and I never remember the right keyboard shortcuts. 
So I built a  simple device so that I can press one big fat arcade button for each of those actions.
![IMG_7282](https://github.com/user-attachments/assets/e70f9911-f114-4600-92f9-e8fb5044c0d4)


The device is simple – three arcade buttons which are connected to an RP2040 Zero microcontroller. _And a button on the side to allow the box to switch between Google Meet and Microsoft Teams mode._
I chose the RP2040 because it is cheap, very small and I am already used to using Raspberry Pi Picos (which would also work well); other microcontrollers may also be suitable but I am not experienced in using them.
The microcontroller runs a simple program that sends the keyboard shortcuts to your computer when a button is pressed, as if it were a keyboard.  
For example, if you press the microphone mute / unmute button then “CTRL+SHIFT+M” _(or "CTRL+D" for Google Meet)_ is sent to your computer which is the mute / unmute shortcut.  
Each button press toggles the LED built into the arcade button between on and off. _When the side switch is pressed, it will activate Teams Mode to use those commands, and toggles the LED on the switch. As the mode is toggled, the Camera, Mute, and Hand arcade buttons are cleared as well._

The program is written in Circuit Python and requires the Adafruit HID Library https://docs.circuitpython.org/projects/hid/en/latest/index.html and https://github.com/adafruit/Adafruit_CircuitPython_Bundle  
You need to copy the library files from the the Adafruit HID Library to your RP2040 / Raspberry Pi Pico library folder and then copy the code.py file from this GitHub.

Full instructions are in the _new Virtual Meetings_ Buttons Instructions PDF file.
The 3D printing files can be found here: https://makerworld.com/en/models/1436571-teams-shortcut-buttons#profileId-1494585  TODO:\\Need to update link to for new file.

I took inspiration from this project: https://github.com/ttan/Mute-o-Matic-V2 - thank you to the author. _Thank you to @TellinStories for the original design and idea._
