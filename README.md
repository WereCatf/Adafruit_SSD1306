# Archived
This fork is no longer needed and will be archived.
Adafruit's upstream nowadays allows for one to define the display's size on-the-fly, instead of requiring one to edit the include-files and allows for one to use a custom TwoWire-instance, making this fork redundant.

# WereCatf_SSD1306

This library has been modified from the Adafruit-original. I got fed up with the idea of having to modify the header-file depending on the display being used,
so this version lets you choose the display-resolution on-the-fly by way of either of below examples:

`WereCatf_SSD1306(int16_t width, int16_t height, int8_t SID, int8_t SCLK, int8_t DC, int8_t RST, int8_t CS);`
`WereCatf_SSD1306(SSD1306_128_64, int8_t SID, int8_t SCLK, int8_t DC, int8_t RST, int8_t CS);`

Valid values are:
	SSD1306_128_64 for 128x64-pixel display
	SSD1306_128_32 for 128x32-pixel display
	SSD1306_96_16 for 96x16-pixel display

You can also use `setI2CPins(int8_t sda, int8_t scl);` to set custom pins to use for I2C on the ESP8266 or ESP32 as long as you call this function *before* `begin()`

----------------------------------------------------------------

This is a library for our Monochrome OLEDs based on SSD1306 drivers

  Pick one up today in the adafruit shop!
  ------> http://www.adafruit.com/category/63_98

These displays use SPI to communicate, 4 or 5 pins are required to  
interface

Adafruit invests time and resources providing this open source code, 
please support Adafruit and open-source hardware by purchasing 
products from Adafruit!

Written by Limor Fried/Ladyada  for Adafruit Industries.  
Scrolling code contributed by Michael Gregg
BSD license, check license.txt for more information
All text above must be included in any redistribution

To download. click the DOWNLOADS button in the top right corner, rename the uncompressed folder Adafruit_SSD1306. Check that the Adafruit_SSD1306 folder contains Adafruit_SSD1306.cpp and Adafruit_SSD1306.h

Place the Adafruit_SSD1306 library folder your <arduinosketchfolder>/libraries/ folder. You may need to create the libraries subfolder if its your first library. Restart the IDE.

You will also have to download the Adafruit GFX Graphics core which does all the circles, text, rectangles, etc. You can get it from
https://github.com/adafruit/Adafruit-GFX-Library
and download/install that library as well 

----------------------------------------------------------------

# Adafruit_SSD1306
<!-- START COMPATIBILITY TABLE -->

## Compatibility

MCU                | Tested Works | Doesn't Work | Not Tested  | Notes
------------------ | :----------: | :----------: | :---------: | -----
Atmega328 @ 16MHz  |      X       |             |            | 
Atmega328 @ 12MHz  |      X       |             |            | 
Atmega32u4 @ 16MHz |      X       |             |            | 
Atmega32u4 @ 8MHz  |      X       |             |            | 
ESP8266            |      X       |             |            | change OLED_RESET to different pin if using default I2C pins D4/D5.
Atmega2560 @ 16MHz |      X       |             |            | 
ATSAM3X8E          |      X       |             |            | 
ATSAM21D           |      X       |             |            | 
ATtiny85 @ 16MHz   |             |      X       |            | 
ATtiny85 @ 8MHz    |             |      X       |            | 
Intel Curie @ 32MHz |             |             |     X       | 
STM32F2            |             |             |     X       | 

  * ATmega328 @ 16MHz : Arduino UNO, Adafruit Pro Trinket 5V, Adafruit Metro 328, Adafruit Metro Mini
  * ATmega328 @ 12MHz : Adafruit Pro Trinket 3V
  * ATmega32u4 @ 16MHz : Arduino Leonardo, Arduino Micro, Arduino Yun, Teensy 2.0
  * ATmega32u4 @ 8MHz : Adafruit Flora, Bluefruit Micro
  * ESP8266 : Adafruit Huzzah
  * ATmega2560 @ 16MHz : Arduino Mega
  * ATSAM3X8E : Arduino Due
  * ATSAM21D : Arduino Zero, M0 Pro
  * ATtiny85 @ 16MHz : Adafruit Trinket 5V
  * ATtiny85 @ 8MHz : Adafruit Gemma, Arduino Gemma, Adafruit Trinket 3V

<!-- END COMPATIBILITY TABLE -->
