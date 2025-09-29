# Overview

The EchoLink is a LoRa device that is able to send off-grid type messages when paired with a bluetooth enabled smartphone. The firmware aspect of the Echolink utilizes Meshtastic, an open source firmware. The hardware aspect of the EchoLink is a custom designed PCB that was created for a small and portable form factor.  A custom designed 3D printed enclosure provides easy access to user buttons/switches while also providing protection to the internal PCB and battery.

![overall_cropped](https://github.com/user-attachments/assets/0deace5f-272d-4df2-a672-4282b56c3c8d)




# Specifications
* LoRa Transceiver: Waveshare Core 1262 HF LoRa Module, SX1262 Chip
* LoRa Antenna: SMA
* LoRa Operation Frequency: 915MHz (US)
* MCU: ESP32-S3-WROOM-1-MCN16R8
* Bluetooth v5.0
* USB Connector: USB-Micro B (for programming and power)
* Battery: 3.7V Li-Poly, 1200mAh
* Battery Charger: Input 5V via USB-Micro B. 500mAh Charge rate.
* Screen: 128x64 OLED Module, 
* GPS: Adafruit Industries ULTIMATE GPS MODULE PA1616D - 66 (integrated antenna)

# Firmware

The Echolink uses the Meshtastic open source firmware. The custom variant used for the EchoLink and its hardware is provided. The latest Meshtastic firmware will have to be downloaded from https://github.com/meshtastic/firmware 
The "echolink" variant will have to be copied into the /variants/esp32s3 folder. When compiling the firmware using VSCode, select the "echolink" environment. 

Detailed instructions on how to customize, compile, and upload the Meashtastic firmware can be found on the official Meshtastic website.  https://meshtastic.org/docs/development/firmware/build/


Once the firmware is uploaded to the Echolink and powered ON, please refer to the Meshtastic open source project website for further details and instructions on how to pair and operate with a bluetooth enabled smartphone device.  
https://meshtastic.org/

# Hardware

<img width="1879" height="888" alt="pcb label_final" src="https://github.com/user-attachments/assets/b26545c8-01b4-4dfe-89a1-0adcbb5995e6" />


The EchoLink is utilizes an ESP32-S3 microcontroller which has integrated wifi and bluetooth connectivity. The small form factor, along with its integrated antenna, also helped minimize the overall size of the EchoLink. The ESP32-S3 was also chosen because of the wide support within the Meshtastic firmware.

The LoRa transceiver comes with an on-board uFL connector. A uFL to SMA connector is used to extend the antenna port from the LoRa module to the top of the case allowing for easy access to the LoRa radio antenna port. 

The GPS module has a dedicated ON/OFF switch to allow for easy toggle of the GPS.

A 3.7V Li-Poly battery is used to supply power to the EchoLink. (NOTE: when selecting battery, make sure to verify polarity of JST connector.)

<img width="1127" height="1050" alt="jst polarity new_final" src="https://github.com/user-attachments/assets/0de7dc15-e3f5-4e7c-8168-f50a673211e2" />



The power circuit utilizes a linear voltage regulator with a fixed output voltage of 3.3V to power all components. To manage the power path between the battery input and USB-Micro B 5V input, a MOSFET power management circuit was implemented. This approach will allow the Echolink to be powered via the internal battery or external 5V input (for charging or power) automatically. 
![Screenshot 2025-05-10 230943](https://github.com/user-attachments/assets/744ef008-2b51-4e1f-9a08-629657d507e3)


There is also an available grove connector which allows for external I2C accessories to be connected.

# Case

The case was designed in Fusion360 and 3D printed using PLA. The simple design of the case allowed for minimal parts and hardware while also allowing access to all user buttons, switches and connections. The case consists of a main body, top cover, and single push button. A single M3x6x5 heat-pressed threaded insert and one M3x20 screw holds the entire case together. If the Grove connector is used, the battery will have to be installed at an angle to avoid interfering with the connector.

NOTE: The current case dimensions and design can only accomodate the 1200mAh 3.7V Li-Poly battery from Adafruit (https://www.adafruit.com/product/258). If using a different battery, please verify that dimensions are similar. 

<img width="1888" height="739" alt="case-bodyTop_label_final" src="https://github.com/user-attachments/assets/00d36fd0-80cf-477c-a198-1b6faaafc319" />




# Resources

https://www.youtube.com/watch?v=zeSlRvCd6tg

https://meshtastic.org/


