# ESP32_PDP11_WROVER
<br>
This is a modified version of a PDP11/40 emulation at https://github.com/Isysxp/PDP11-on-the-M5-Core<br>
This app requires an ESP32 processor with at least 512K of PSRAM.<br>
An SDCard: #define SCK  14, #define MISO  2, #define MOSI  15, #define CS  13 (as on WROVER kit)<br>
The build enviroment is for the current Arduino IDE V 2.3.1 or the VisualMicro plugin for Visual Studio.<br>
The critical libraries required are:<br>
Adafruit TinyUSB, SDFAT-Adafruit Fork, ESPTelnetStream (https://github.com/LennartHennigs/ESPTelnet)<br>
and Espressif Arduino-esp32 (https://github.com/espressif/arduino-esp32).<br>
Disk images: I strongly suggest that these are configued in SIMH and then copied to the SDCard. THis app also
supports more that 1 RL01/2 drives. This is achieved by concatenating the disk images having verified that the images
are RL01:5243392 RL02:10486272 bytes in length. These are standard SIMH image sizes for the RL drives. (See rl11.cpp)<br>
The image selection and console are accesible via a single USB port that should appear when the ESP32 is started.<br>
The app provides 1 telnet stream linked to a DL11 serial port mapped at 2 Unibus addresses: 0775610 and 0776500 Vector:0300.<br>
(Do not try to use both at once!)<br>
<br>
Ian Schofield April 2024<br>

