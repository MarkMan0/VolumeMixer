# The VolumeMixer Project

<img src="VolumeMixer_board/images/demo.gif" alt="demo" width="400px"/>

## Why
Changing the volume of some apps is troublesome and requires switching to the application to change its volume. In some cases, it's not trivial to change the volume in the app itself. This device will allow you to change the volume of applications in an external display, as you would in the built-in volume mixer.

I've found a similar project, [deej](https://github.com/omriharel/deej), but I wanted something dynamic - it shows the apps that are currently open. I had an STM32F4 lying around, with a touch LCD, so I decided to make my own.

This device will monitor the open audio sessions, display their icons and control the volume of each one of them.

## Structure

The project has 2 parts - the embedded device and the PC application. The embedded device is programmed in Platformio, and use HAL libraries. The PC app uses CMake and WinAPI to gather data about the volume sessions of the running applications on the PC.

Take a look at the READMEs in the PC and board projects to learn more.

## TODO

1. Replace polling with notification
1. Add basic multimedia control
1. Add functionality to monitor system load, temperatures etc.
1. Create enclosure
1. Use potentiometers to change volume - the touch control is weird and requires a sturdy base
