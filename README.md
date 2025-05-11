# Overview
The EchoLink is a LoRa device that is able to send off-grid type messages. The firmware aspect of the Echolink utilizes Meshtastic, an open source firmware. The hardware aspect of the Echolink is a custom designed PCB that was created for a small and portable form factor. A 3D printed enclosure provides easy access to user buttons while also providing protection to the internal PCB and battery. 

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
The Echolink uses the Meshtastic open source firmware. The custom firmware used for the EchoLink and its hardware is provided. Instructions on how to customize the Meashtastic firmware were followed from the official Meshtastic website https://meshtastic.org/docs/development/firmware/build/

Provided in the firmware folder is the latest Meshtastic firmware build. Also provided is the custom variant that was used for the EchoLink. 

# Hardware
![pcb](https://github.com/user-attachments/assets/914ace8b-9561-488f-bc49-256502ea235c)

The EchoLink is utilizes an ESP32-S3 microcontroller which has integrated wifi and bluetooth connectivity. The small form factor, along with its integrated antenna, also helped minimize the overall size of the EchoLink. The ESP32-S3 was also chosen because of the wide support within the Meshtastic firmware.

The GPS module has a dedicated ON/OFF switch to allow for easy toggle of the GPS.

A 3.7V Li-Poly battery is used to supply power to the EchoLink. The power circuit utilizes a linear voltage regulator with a fixed output voltage of 3.3V to power all components. To manage the power path between the battery input and USB-Micro B 5V input, a MOSFET power management circuit was implemented. This approach will allow the Echolink to be powered via the internal battery or external 5V input (for charging or power) automatically. 
![Screenshot 2025-05-10 230943](https://github.com/user-attachments/assets/744ef008-2b51-4e1f-9a08-629657d507e3)






