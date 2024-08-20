<!---[![License: MIT](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/justcallmekoko/ESP32Marauder/blob/master/LICENSE)--->
# DIY Wifi Addon Module for Flipper Zero Instructions
## Credits and More Info
More info about this project can be found at the [wifi marauder wiki](https://github.com/justcallmekoko/ESP32Marauder/wiki)

## Required parts
<img width="586" alt="parts-photo-numbered" src="https://github.com/user-attachments/assets/b780d4bd-b7f2-4876-a0f3-873f49cbf78c">

1. Flipper Zero
2. Micro SD Card - **FAT-32 formatted** 
3. 10+8 Square Pin Headers (Come with your Lilygo T8 ESP32-S2)
4. 10x24 Protoboard
5. 2x20 [round female headers](https://www.aliexpress.com/item/4001122376295.html)

6. [Lilygo T8 ESP32-S2](https://www.lilygo.cc/products/esp32-s2)

7. 2x20 [round male pin headers](https://www.aliexpress.com/item/4001122376295.html)

## Wiring and Soldering

### Wiring Diagram
<img width="400" alt="wiring-diagram-aligned-colored" src="https://github.com/user-attachments/assets/d97f77cb-b043-4822-9d8a-3fd4223d15be">

### Picture proto board top
<img width="586" alt="solder-top" src="https://github.com/user-attachments/assets/ea689666-8785-44c8-941b-9e3af013207c">

### Picture proto board bottom
<img width="586" alt="solder-proto-bottom" src="https://github.com/user-attachments/assets/cf98c78e-11d6-4d50-a264-f94350de9e44">

### ESP32-S2 board Assembled
![image](https://github.com/user-attachments/assets/c5073fa0-0c43-43f2-b1c1-df5d7e8e2436)

## After soldering
After soldering (or before) you should install the forked marauder firmware on your esp32:

### Flashing the esp32-s2
* go to https://esp.huhn.me/ and 
* Connect Device
* Select the latest [esp32_marauder.ino.bootloader.bin](https://github.com/ko-lab/ESP32Marauder_ESP32_S2_DIY/releases/latest/download/esp32_marauder.ino.bootloader.bin) file at 0x1000.
* Select the latest [esp32_marauder.ino.partitions.bin](https://github.com/ko-lab/ESP32Marauder_ESP32_S2_DIY/releases/latest/download/esp32_marauder.ino.partitions.bin) file at 0x8000.
* Select the lateast [esp32_marauder.ino.bin](https://github.com/ko-lab/ESP32Marauder_ESP32_S2_DIY/releases/latest/download/esp32_marauder.ino.bin) file at 0x10000.
* Note: some people had to flash 2 times before it worked.


#### esp web flasher correct settings:
<img width="586" alt="esp-web-flasher-settings-screenshot" src="https://github.com/user-attachments/assets/4a5b0e71-7a89-4c6c-8d36-b31c951d55db">



### Installing the Marauder app
If your flipper zero firmware does not have the [ESP32] Wifi Marauder app yet, you shoul install this first. App is here https://lab.flipper.net/apps/esp32_wifi_marauder, you can install it with an app or by putting the fap on your flipper sd card.

### Using it
Then to use it follow these steps.

* start the Wifi Marauder app
 * if the power wiring is correct, then you will see a blue and red light on the esp32. 
* **Press the reset button on the LILIGY T8 now**
* then try `scan [ap]` for example, it should start printing ssid's

### Using the SD Card
One of the nice things about the Lilygo T8 ESP32-S2 board from this workshop is that it comes with a TF card slot on top. This allows us to
- Write pcap files from sniffing
- Store Evil portal HTML files

**But to use it, you will first need to format it as fat32**
