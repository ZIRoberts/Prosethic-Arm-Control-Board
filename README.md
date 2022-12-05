# Prosethic Arm Control (P.A.C) Board

Here exists all PCB designs and electrical schematics for the DIY Electromyographic Prosethic Arm. All symbols, schematics, footprints, and board layouts are designed in Altium. 

# Overview

There is a single board in this sytem and it is broken up into three sections represented by their own respeitive schematic sheet. The first section is microcontroller connections and power regulation. This sheet includes the microcontroller, 5 V Buck Regulator, and two EMI filters for the 3V3 and 5V lines. The MCU used for this project is the ESP32-S2 by Espressiff Systems. This microcontroller was sekected because it was of appropriate size, had appropriate pin count, has a configurable three speed processor (80 MHz, 160 MHz, or 240 MHz), compatable with Arduino libraries, and the creator already had experience using this family of microcontrollers. 

The second section is the Low End Current Sense circuit. This is used to sense the current consumption of each motor and is used give the MCU feedback on the current state of the motors, ensure the motors do not enter stall, and to check of an object is within the hand. The current sensor response will also be used to verify the input of the feed back connectors discuessed in the next section.  

The third section is Feedback sensors and connectors. This section houses all of the connectors used to interface with all the external components including servo motors, eletromyographic sensors, batteries, and the feedback sensors. The the feedback sensors are force sensative resistors placed on the tip of each finger and palm of the hand. This is to create a closed loop feedback system by relaying the force applied to an object to the microcontroller. The batteries consist of two 18650 Lithium-ion cells connected in series. This configuration capabale of powering the system for upwards of 18 hours on a single charge. 

A full list of electronic components can be found in the Bill of Materials.xlsx and images of the design can be found below.

# Schematic
## Microcontroller Power Sheet
![Microcontroller_Power Sheet](https://user-images.githubusercontent.com/49044136/205477574-a3dd425d-cf8c-4f5e-bab4-c07542127ff5.png)
## Current Sense Sheet
![Current Sense sheet](https://user-images.githubusercontent.com/49044136/205477589-91933f67-34e2-4358-af3d-e4d87e769c6b.png)
## Connectors Sheet
![Connectors sheet](https://user-images.githubusercontent.com/49044136/205477596-1d0d640e-c56b-4eee-aea8-f74eddb341b0.png)

# PCB Layout
## Top Copper
![Front Copper](https://user-images.githubusercontent.com/49044136/205477656-8e42e34b-dd75-43ee-9f2b-0ec3aba00bb1.png)
## Bottom Copper
![Back copper](https://user-images.githubusercontent.com/49044136/205477662-ded94ca8-ce4d-48af-a675-c6c8e50ff81b.png)

# 3D Render
## Top View
![PCB BACK 3D](https://user-images.githubusercontent.com/49044136/205477670-dd9c9b01-b8f1-4e46-ba3c-b9c282a79933.png)
## Bottom View
![PCB BACK 3D RENDER](https://user-images.githubusercontent.com/49044136/205477678-5a4fa943-6b0f-4d79-8838-1e27ebff38d8.png)
