# Prosethic Arm Control (P.A.C) Board

Here exists all PCB designs and electrical schematics for the DIY Electromyographic Prosethic Arm. All symbols, schematics, footprints, and board layouts are designed in Altium. 

![Isometic_Render 2](https://user-images.githubusercontent.com/49044136/221460442-274faa0b-ac6e-4554-932c-4927e1d84266.png)

# Overview

There is a single board in this sytem and it is broken up into four sections represented by their own respective schematic sheet. The first section is microcontroller connections and power regulation. This sheet includes the microcontroller, 5 V Buck Regulator, and two EMI filters for the 3V3 and 5V lines. The MCU used for this project is the ESP32-S2 by Espressiff Systems. This microcontroller was selected because it was of appropriate size, had appropriate pin count, has a configurable three speed processor (80 MHz, 160 MHz, or 240 MHz), compatable with Arduino libraries, and the creator already had experience using this family of microcontrollers. 

The second section is the Low End Current Sense circuit. This is used to sense the current consumption of each motor and is used give the MCU feedback on the current state of the motors, ensure the motors do not enter stall, and to check of an object is within the hand. The current sensor response will also be used to verify the input of the feed back connectors discuessed in the next section.  

The third second is the external ADC and all of the periphial connections. The ADC impleneted into the controller is the MAX11629EEE+. It is used to acquire output of the current sense circuit, and data from the electromyographic sensor. An external precision 3V reference is used to allow a wide range of ADC measurments and a power filter to ensure noise from the rest of the circuit does not impact the measurements.

The fourth section is Feedback sensors and connectors. This section houses all of the connectors used to interface with all the external components including servo motors, eletromyographic sensors, batteries, and the feedback sensors. The the feedback sensors are force sensative resistors placed on the tip of each finger and palm of the hand. This is to create a closed loop feedback system by relaying the force applied to an object to the microcontroller. The batteries consist of two 18650 Lithium-ion cells connected in series. This configuration capabale of powering the system for upwards of 18 hours on a single charge. 

A full list of electronic components can be found in the Bill of Materials.xlsx and images of the design can be found below.

# Schematic
## Microcontroller Power Sheet
![Microcontroller_Power_Sheet PDF](https://user-images.githubusercontent.com/49044136/221460759-57aa486f-f31d-4ff7-8519-8166479615d1.png)
## Current Sense Sheet
![Current_Sense_Sheet PDF](https://user-images.githubusercontent.com/49044136/221460783-f48b2285-11f6-4511-be26-3b7db4b9864f.png)
## ADC Connections Sheet
![ADC_Connections_Sheet PDF](https://user-images.githubusercontent.com/49044136/221460799-eacca5ba-04ef-49fc-b309-29b517653676.png)
## Connectors Sheet
![Connectors_Sheet PDF](https://user-images.githubusercontent.com/49044136/221461522-7211f050-7786-4567-96b1-6cd52167aed2.png)


# PCB Layout
## Top Copper
![Top_Copper](https://user-images.githubusercontent.com/49044136/221460137-322c9766-5168-4325-9550-f34b93c86b3a.png)
## Bottom Copper
![Bottom_Copper](https://user-images.githubusercontent.com/49044136/221460150-f54cbd75-96f1-4ce5-a674-4cd8282e6a54.png)

# 3D Render
## Top View
![Bottom_Render](https://user-images.githubusercontent.com/49044136/221460174-1b65c761-02fe-47d1-9417-00c6a91dd13f.png)
## Bottom View
![Top_Render](https://user-images.githubusercontent.com/49044136/221460184-d3eff1ab-9e2c-4da6-9c2a-788d1391a4c6.png)

