# STM8-RDA5807-RADIO-in-assembly

The code is written in ST assembler in STvisual developer tool provided by STM.
The code initialises the RDA5807 chip and provides subroutines to tune upwards,
tune downwards, seek upwards, seek downwards , bass boost on/off  and save current
channel to eeprom as favourite. The favourite channel is used as default value on
powerup. Total 6 push switches are connected between pd1......pd6 to the ground
to achive the above actions. ssd1306 OLED is used to display the channel value
with stretched fonts. Only minimum fonts (16x8) are used to save ROM and the bigger
size is achived by stretching it to 32x16.
