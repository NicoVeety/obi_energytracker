# Obi Energy Tracker Hardware Overview

### Table of contents
[1. Transmitter](#Transmitter)  
[2. Reciver](#Reciver)  

## Transmitter
Text

<img width="300" alt="FrontPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Transmitter/IMG_3590%20-%20Kopie.jpeg">
<img width="300" alt="IC" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Transmitter/IMG_3593%20-%20Kopie.jpeg">
<img width="300" alt="BackPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Transmitter/IMG_3594%20-%20Kopie.jpeg">

## Reciver

Hardware:

ESP32-C3-WROOM-02

Ra-03SCH LoRa Module

ESP32 Pinout:
| Function             | ESP Pin | ESP Pin | Function            |
|----------------------|---------|---------|---------------------|
| V+                   | 3V3     | IO0     | LED                 |
| Debug Header EN      | EN      | IO1     | LoRa BUSY           |
| LoRa CTL1            | IO4     | IO2     | LoRa MISO           |
| LoRa CTL2            | IO5     | IO3     | LoRa DIO2           |
| LoRa SCK             | IO6     | IO19    | LoRa DIO1           |
| LoRa MOSI            | IO7     | IO18    | LoRa RST            |
|                     | IO8     | TXD     | Debug Header TXD    |
| Debug Header BOOT    | IO9     | RXD     | Debug Header RXD    |
| GND                  | GND     | IO10    | LoRa NSS            |


ESP32 Daugtherboard:
| Left Pin | Right Pin |
|----------|-----------|
| 3V3      | IO0       |
| EN       | IO1       |
| IO4      | IO2       |
| IO5      | IO3       |
| IO6      | IO19      |
| IO7      | IO18      |
| Switch   | TXD       |
| IO9      | RXD       |
| GND      |           |
| IO10     |           |


```Initial Boot Log:
Build:Feb  7 2021
rst:0x1 (POWERON),boot:0xd (SPI_FAST_FLASH_BOOT)
SPIWP:0xee
mode:DIO, clock div:1
load:0x3fcd6100,len:0x1180
load:0x403ce000,len:0x750
load:0x403d0000,len:0x2b0c
entry 0x403ce000
system start! soft versoin:1.0.1(58) hardware version:6,
W (601) BTDM_INIT: esp_bt_controller_mem_release not implemented, return OK
```
```reboot and no Server reachable Log
rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:1
load:0x3fff0030,len:4876
ho 0 tail 12 room 4
load:0x40078000,len:16560
load:0x40080400,len:3500
entry 0x400805b4
W (30031) BT_HCI: hcif disc complete: hdl 0x1, rsn 0x13
W (188971) wifi:<ba-add>idx:0 (ifx:0, *MAC), tid:0, ssn:3, winSize:64
W (204111) wifi:<ba-add>idx:1 (ifx:0, *MAC), tid:6, ssn:2, winSize:64
E (210281) esp-tls: couldn't get hostname for :iot-core.companioninnovations-prd.obi.solutions: getaddrinfo() returns 202, addrinfo=0x0
E (210281) esp-tls: Failed to open new connection
E (210281) TRANSPORT_BASE: Failed to open a new connection
E (210291) MQTT_CLIENT: Error transport connect
W (215291) MQTT_CLIENT: Client asked to stop, but was not started
```
```Boot with normal Operation:
ESP-ROM:esp32c3-api1-20210207
Build:Feb  7 2021
rst:0x3 (RTC_SW_SYS_RST),boot:0xd (SPI_FAST_FLASH_BOOT)
Saved PC:0x40380690
SPIWP:0xee
mode:DIO, clock div:1
load:0x3fcd6100,len:0x1180
load:0x403ce000,len:0x750
load:0x403d0000,len:0x2b0c
entry 0x403ce000
system start! soft versoin:1.0.2(67) hardware version:6
W (6845) wifi:<ba-add>idx:0 (ifx:0, *MAC), tid:0, ssn:2, winSize:64
W (7855) wifi:<ba-add>idx:1 (ifx:0, *MAC), tid:6, ssn:2, winSize:64
```


All Grid Power Devices removed to directly connect

<img width="300" alt="FrontPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Reciver/IMG_3599%20-%20Kopie.jpeg">
I connected an JST Connector for Debugging to one of my Devices

<img width="300" alt="BackPCB" src="https://github.com/NicoVeety/obi_energytracker/blob/71d78aa692d4290a7b2c5d8212ac8ee406ee625d/Reciver/IMG_3600%20-%20Kopie.jpeg">

