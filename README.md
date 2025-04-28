# Overview
The EchoLink is a LoRa device that is able to send off-grid type messages. The firmware aspect of the Echolink utilizes Meshtastic, an open source firmware. The hardware aspect of the Echolink is a custom designed PCB that was created for a small and portable form factor. A 3D printed enclosure provides easy access to user buttons while also providing protection to the internal PCB and battery. 

# Specifications
*LoRa Transceiver: Waveshare Core 1262 HF LoRa Module, SX1262 Chip
*LoRa Antenna: SMA
*LoRa Operation Frequency: 915MHz (US)
*MCU: ESP32-S3 -WROOM-1-MCN16R8
*Bluetooth v5.0
*USB Connector: USB-Micro B (for programming and power)
*Battery: 3.7V Li-Poly, 1200mAh
*Battery Charger: Input 5V via USB-Micro B. 500mAh Charge rate.
*Screen: 128x64 OLED Module, 
*GPS: Adafruit Industries ULTIMATE GPS MODULE PA1616D - 66 (integrated antenna)

# Firmware
The Echolink uses the Meshtastic open source firmware. The custom firmware used for the EchoLink and its hardware is provided. Instructions on how to customize the Meashtastic firmware were followed from the official Meshtastic website https://meshtastic.org/docs/development/firmware/build/

Provided in the firmware folder is the latest Meshtastic firmware build. Also provided is the custom variant that was used for the EchoLink. 

# Hardware
