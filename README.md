<!---[![License: MIT](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/justcallmekoko/ESP32Marauder/blob/master/LICENSE)--->
# DIY Wifi Addon Module for Flipper Zero Instructions
## Credits and More Info
More info about this project can be found at the [wifi marauder wiki](https://github.com/justcallmekoko/ESP32Marauder/wiki)

## Connection diagram
<img width="514" alt="wiring_diagram" src="https://github.com/user-attachments/assets/2874adcb-a04a-425d-b31f-82fac62428e9">


## Connection pictures
### Proto board top
![solder-top](https://github.com/user-attachments/assets/ea689666-8785-44c8-941b-9e3af013207c)
### Proto board bottom
![proto-bot](https://github.com/user-attachments/assets/cf98c78e-11d6-4d50-a264-f94350de9e44)
### ESP32-S2 board

### Assembled
![image](https://github.com/user-attachments/assets/c5073fa0-0c43-43f2-b1c1-df5d7e8e2436)

# Afer soldering
After soldering (or before) you should install the forked marauder firmware on your esp32:

## Flashing the esp32-s2
* go to https://esp.huhn.me/ and 
* Connect Device
* Select the latest [esp32_marauder.ino.bootloader.bin](https://github.com/ko-lab/ESP32Marauder_ESP32_S2_DIY/releases/latest/download/esp32_marauder.ino.bootloader.bin) file at 0x1000.
* Select the lateast [esp32_marauder.ino.bin](https://github.com/ko-lab/ESP32Marauder_ESP32_S2_DIY/releases/latest/download/esp32_marauder.ino.bin) file at 0x10000.
* Note: some people had to flash 2 times before it worked.
* 
## esp web flasher correct settings:
<img width="1783" alt="Screenshot 2024-08-17 at 20 33 16" src="https://github.com/user-attachments/assets/65a3c6d0-a2c9-4339-b5a8-8e1155bd8270">


## Installing the Marauder app
If your flipper zero firmware does not have the [ESP32] Wifi Marauder app yet, you shoul install this first. App is here https://lab.flipper.net/apps/esp32_wifi_marauder, you can install it with an app or by putting the fap on your flipper sd card.

## Using it
Then to use it follow these steps.

* start the Wifi Marauder app
 * if the power wiring is correct, then you will see a blue and red light on the esp32. 
* ** Press the reset button on the esp32s2 now **
* then try `scan [ap]` for example, it should start printing ssid's

 ### Using the SD Card
You can use the sd card for more efficiently storing pcap files from sniffing results.
**But to use it, you will first need to format it as fat32**
