---
layout: page
title: ATMega32 Mp3 Player
permalink: /node/11/
description: "An Mp3 player based on the atmega32 and the vs1003 decoder chip that reads the content from an SD card."
---

# AVR ATMega32 Mp3 Player

This is a project I completed for a microcontroller programming class where we had to program an AVR microcontroller. For the purpose of this project we used an ATMega32 on which we are using 13KB of flash memory. The implementation is in C and the compiler used was gcc.

For programming the controller we used the usbasp programmer that is using JTAG and was quite simple to setup on linux. There is no external crystal on the system since it is not critical to be precise for any of the operations we perform. We are running at 8Mhz since this is an adequate frequency for streaming the mp3 data to the decoder and have no playback delays.

## Hardware Components:

* ATMega32 on a development board with exposed I/O Pins
* VS1003 MP3 decoder development board with all the circuitry around the chip
* Nokia 5510 screen
* SD Card connector
* 6 push buttons, a strip board and some cables

You can find all the source code of the project below which you can in turn use as sample code for your own projects smiley. The code sections I have written is under GPL, but the components I used from other projects are re-distributed with no license (since they had no license from the beginning).



## Schematic of the circuit:

I have omitted several parts in the circuit(i.e. all the components of the development boards etc.), just want to show how the external components are connected to the microcontroller's GPIOs.

![alt text](/assets/data/avrmp3player/schematic.png)

## Pictures of Prototype:

![alt text](/assets/data/avrmp3player/mp3_1.jpg)
![alt text](/assets/data/avrmp3player/mp3_2.jpg)
![alt text](/assets/data/avrmp3player/mp3_3.jpg)

Source code available for download from [here](/assets/data/avrmp3player/Mp3Player.zip).
