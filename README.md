# STM8-RDA5807-RADIO-in-assembly

The code is written in ST assembler in STvisual developer tool provided by STM.
The code initialises the RDA5807 chip and provides subroutines to tune upwards,
tune downwards, seek upwards, seek downwards , bass boost on/off  and save current
channel to eeprom as favourite. The favourite channel is used as default value on
powerup. Total 6 push switches are connected between pd1......pd6 to the ground
to achive the above actions. ssd1306 OLED is used to display the channel value
with stretched fonts. Only minimum fonts (16x8) are used to save ROM and the bigger
size is achived by stretching it to 32x16.
The version 1 has codes that fixes issues with no audio on initial start up with channel value
loaded from memory. The audio is not output until the tune is moved up or down atleast
 by 1 khz. Once the tune is increased and then decreased by 1 space/1khz the audio issue 
 is rectified. version 1 has this added, The ZIP file is the whole stvd project with
 all executables. can be used to program the chip with STvisual programmer and stlink.
 PB5 - SDA
 pB4 -sck
 PD2 = seek_up
 PD3 = seek_down
 PD4 = tune_up
 PD5 = tune_down
 PD6 = bass_on
 PD1 = store_station
