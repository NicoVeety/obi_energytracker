# Obi Energy Tracker Hardware Overview

## Transmitter
Text

<img width="300" alt="FrontPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Transmitter/IMG_3590%20-%20Kopie.jpeg">
<img width="300" alt="IC" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Transmitter/IMG_3593%20-%20Kopie.jpeg">
<img width="300" alt="BackPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Transmitter/IMG_3594%20-%20Kopie.jpeg">

## Reciver

Hardware:
ESP32-C3-WROOM-02
Ra-03SCH

ESP32 Pinout:
                           ESP
V+                : 3V3     |   IO0   : LED
Debug Header EN   : EN      |   IO1   : LoRa BUSY
LoRa CTL1         : IO4     |   IO2   : LoRa MISO
LoRa CTL2         : IO5     |   IO3   : LoRa DIO2
LoRa SCK          : IO6     |   IO19  : LoRa DIO1
LoRa MOSI         : IO7     |   IO18  : LoRa RST
                  : IO8     |   TXD   : Debug Header TXD
Debug Header BOOT : IO9     |   RXD   : Debug Header RXD
GND               : GND     |   IO10  : LoRa NSS


ESP32 Daugtherboard:

3V3       |   IO0
EN        |   IO1
IO4       |   IO2
IO5       |   IO3
IO6       |   IO19
IO7       |   IO18
Switch    |   TXD
IO9       |   RXD
GND     
IO10    

All Grid Power Devices removed to directly connect
<img width="300" alt="FrontPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Reciver/IMG_3599%20-%20Kopie.jpeg">
I connected an JST Connector for Debugging to one of my Devices
<img width="300" alt="BackPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Reciver/IMG_3600%20-%20Kopie.jpeg">

