# cam86 software

This page discusses the software elements of the Camera

## ATMeg328 firmware

* See this [great article on programming the ATmeg328](https://davecturner.github.io/2019/02/23/programming-avr-microcontrollers.html)
using In System Programming (ISP)
* The above article also discusses the use of the AVR toolchain to compile firmware on a Raspberry Pi
* Source code for the CAM86 firmware can be found [here](https://github.com/axsdenied/cam86_fw)
* Fuses ??

## EEProm programming

* The EEProm on the camera controller board is used to configure the USB interface and requires pre-programming
* still researching this

## Camera control software

* The CAM86 development community used Windows as the development platform
* Efforts were focused around an [ASCOM standard](https://ascom-standards.org/)
* The [Windows ASCOM driver source](https://github.com/axsdenied/cam86_dll) is written in Delphi and the community support for the code appears to be limited

