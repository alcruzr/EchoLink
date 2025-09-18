# Overview
The EchoLink is a LoRa device that is able to send off-grid type messages when paired with a bluetooth enabled smartphone. The firmware aspect of the Echolink utilizes Meshtastic, an open source firmware. The hardware aspect of the EchoLink is a custom designed PCB that was created for a small and portable form factor. The custom PCB allows for two different configurations of the EchoLink device. Configuration 1 utilizes a custom 3D printed enclosure that provides easy access to user buttons/switches while also providing protection to the internal PCB and battery. Configuration 2 utilizes a tin container as the device enclosure, along with the CardKB Mini Keyboard by M5STACK (not included), which allows for a stand-alone device configuration that does not need a paired smartphone to send/receive messages.

[pic]

# Specifications
* LoRa Transceiver: Waveshare Core 1262 HF LoRa Module, SX1262 Chip
* LoRa Antenna: SMA
* LoRa Operation Frequency: 915MHz (US)
* MCU: ESP32-S3-WROOM-1-MCN16R8
* Bluetooth v5.0
* USB Connector: USB-C (for programming and charging)
* Battery: 3.7V Li-Poly, 1200mAh
* Battery Charger: Input 5V via USB-C. 500mAh Charge rate.
* Screen: 128x64 OLED Module, 
* GPS: Adafruit Industries ULTIMATE GPS MODULE PA1616D-66 (integrated antenna)

# Firmware
The Echolink uses the Meshtastic open source firmware. The custom variant used for the EchoLink and its hardware is provided. The latest Meshtastic firmware will have to be downloaded from https://github.com/meshtastic/firmware 
The "echolink" variant will have to be copied into the /variants/esp32s3 folder. When compiling the firmware using VSCode, select the "echolink" environment. 

Detailed instructions on how to customize, compile, and upload the Meashtastic firmware can be found on the official Meshtastic website.  https://meshtastic.org/docs/development/firmware/build/

Once the firmware is uploaded to the Echolink device and powered ON, please refer to the Meshtastic open source project website for further details and instructions on how to pair and operate with a bluetooth enabled smartphone device.  
https://meshtastic.org/

# Hardware

<img width="1879" height="888" alt="pcb label_final" src="https://github.com/user-attachments/assets/b26545c8-01b4-4dfe-89a1-0adcbb5995e6" />


The EchoLink utilizes an ESP32-S3 microcontroller, which has integrated wifi and bluetooth connectivity. The small form factor, along with its integrated antenna, also helped minimize the overall size of the EchoLink device. The ESP32-S3 was also chosen because of the wide support within the Meshtastic firmware.

The LoRa transceiver comes with an on-board uFL connector. 

The GPS module and integrated buzzer each have a dedicated ON/OFF switch to allow for easy toggle of the GPS and buzzer.

A 3.7V Li-Poly battery is used to supply power to the EchoLink device. (NOTE: When selecting a battery, make sure to verify polarity of JST connector. There are four jumper pads on the back of the device which allows the user to select which battery polarity JST connector is used. CAUTION: BEFORE CONNECTING THE BATTERY, MAKE SURE THE CORRECT POLARITY IS SELECTED ON THE PCB.)

<img width="1127" height="1050" alt="jst polarity new_final" src="https://github.com/user-attachments/assets/0de7dc15-e3f5-4e7c-8168-f50a673211e2" />



The power circuit utilizes a linear voltage regulator with a fixed output voltage of 3.3V to power all components. To manage the power path between the battery input and USB-C 5V input, a MOSFET power management circuit was implemented. This approach will allow the Echolink device to be powered via the internal battery or external 5V input (for charging or power) automatically. 
![Screenshot 2025-05-10 230943](https://github.com/user-attachments/assets/744ef008-2b51-4e1f-9a08-629657d507e3)

There is also an available grove connector which allows for external I2C accessories to be connected.

# Confugurations
Config 1:

The case was designed in Fusion360 and 3D printed using PLA. The simple design of the case allowed for minimal parts and hardware while also allowing access to all user buttons, switches and connections. The case consists of a main body, top cover, and single push button. A single M3x6x5 heat-pressed threaded insert and one M3x20 screw holds the entire case together. If the Grove connector is used, the battery will have to be installed at an angle to avoid interfering with the connector.
[pic]

NOTE: The current case dimensions and design can only accomodate the 1200mAh 3.7V Li-Poly battery from Adafruit (https://www.adafruit.com/product/258). If using a different battery, please verify that dimensions are similar. 

<img width="1888" height="739" alt="case-bodyTop_label_final" src="https://github.com/user-attachments/assets/00d36fd0-80cf-477c-a198-1b6faaafc319" />



Config 2:

The EchoLink can also be configured to fit in a 4"x3"x1" plsatic enclosure that is easily purchased on amazon (link). The PCB allows for the OLED display to be mounted horizontally for this configuration. NOTE: when soldering the buzzer to the PCB, make sure it is moved as far down as possible to avoid interference with the OLED display
[pic: buzzer and OLED]

The CardKB mini keyboard is attached to the lid of the box with double sided tape and the included Grove connector is used to connect to the EchoLink. The Grove cable wires are soldered to the extra OLED pads on the EchoLink. Provided is a stl file for a cable retainer that can be mounted on the lid of the box to provide a cleaner look. 
[pic]

Provided is a stl file for the insert that will allow the EchoLink to be easily mounted inside the box. A washer (stl provided), single M3 screw insert, and screw is used to mount the EchoLink to the insert. Some double sided tape is used to mount the insert to the inside of the box. 
[pic: tape on bottom]

Provided on the insert is a holder for a SMA connector.
[pic]

The insert was designed to be flexible and a tab is provided to allow the user to pull up and be able to access the USB-C connector for charging/programming. 
[pic]

NOTE: The current case dimensions and design can only accomodate the 1200mAh 3.7V Li-Poly battery from Adafruit (https://www.adafruit.com/product/258). If using a different battery, please verify that dimensions are similar.

# Resources

https://www.youtube.com/watch?v=zeSlRvCd6tg

https://meshtastic.org/


