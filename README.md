# Tuning Fork Clock

This repository contains all the files for the Tuning Fork Clock PCB and 3D printed parts.

The PCB was designed for home etching, so the traces are very wide and
the via dimater has been increased so wires can be soldered in to make connections between the layers.

All external connections are broken out on an edge connector at the top that serves as solder pads for making connections.

The "fork mount" directory contains the CAD and STL files for the tuning fork mounting hardware.  
Two 22mH inductors and a 15x5mm neodymium magnet need to be inserted into the base part of the mount.

The polarity of the inductors is not consistent from the factory, so some experimentation is required to get the best results.  
Usually flipping one inductor or the magnet will result in much better vibration of the fork.

The on-board BNC connector can be connected to a scope to observe the output waveform of the pickup.

Check out the [YouTube video](https://www.youtube.com/watch?v=TgB_1jr5b_c) for more info on how it all works.

Also check out [this repository](https://github.com/NuclearLighthouseStudios/Tuning-Fork-Clock-Firmware) for the firmware.

| Reference                                         | Quantity | Value         | Description                                          |
| :------------------------------------------------ | -------: | ------------: | :--------------------------------------------------- |
| C1 C4 C5 C9 C102 C103 C104 C105 C106 C107         | 10       | 100n          | Generic ceramic capacitor                            |
| C101                                              | 1        | 100µ          | Electrolytic capacitor, 16V                          |
| C2 C3                                             | 2        | 47n           | Generic ceramic capacitor                            |
| D1                                                | 1        | 1N4148        | DO-35 Diode                                          |
| D2 D3 D4                                          | 3        |               | 5mm LED                                              |
| J3                                                | 1        |               | Panel Mount BNC Connector                            |
| Q1 Q2 Q3 Q4 Q5 Q6 Q7                              | 7        | BC547B        | 0.1A Ic, 45V Vce, Small Signal NPN Transistor, TO-92 |
| R1 R7 R12 R13 R14 R15 R16 R17 R18 R19 R25 R26 R27 | 13       | 1k            | Metal film resistor 1%, DIN 0207, Horizontal         |
| R2 R6                                             | 2        | 1M            | Metal film resistor 1%, DIN 0207, Horizontal         |
| R20 R21 R22 R23 R24                               | 5        | 10k           | Metal film resistor 1%, DIN 0207, Vertical           |
| R3                                                | 1        | 4.7k          | Metal film resistor 1%, DIN 0207, Horizontal         |
| R4 R5 R10                                         | 3        | 10k           | Metal film resistor 1%, DIN 0207, Horizontal         |
| R8 R9                                             | 2        | 100k          | Metal film resistor 1%, DIN 0207, Horizontal         |
| SW1                                               | 1        |               | Alps EC12E Rotary Encoder with Switch, Vertical      |
| U1                                                | 1        | NE555P        | Precision Timers, 555 compatible, PDIP-8             |
| U10                                               | 1        | 440Hz         | Tuning Fork in 3D printed mount                      |
| U10                                               | 2        | 22mH          | 11mm diameter inductor                               |
| U10                                               | 1        |               | 15x5mm neodymium rod magnet                          |
| U2                                                | 1        | ATtiny4313-PU | 8-Bit Microcontroller, 20Mhz, 4k Flash, 256b RAM     |
| U3                                                | 1        | 74HC595       | 8−Bit shift register                                 |
| U4 U5 U6 U7 U8                                    | 5        | SC39-11YWA    | 7 Segment Display                                    |
| U9                                                | 1        | L7805         | 5V voltage regulator, TO-220                         |
