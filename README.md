# SMA-Q2_replacement_board
![SMA-Q2_replacement_board](https://github.com/BigCorvus/SMA-Q2_replacement_board/blob/master/20191017_114838.jpg)
![SMA-Q2_replacement_board](https://github.com/BigCorvus/SMA-Q2_replacement_board/blob/master/SMA_Q2_nrf52840.png)
Custom replacement board with an nrf52840 module based on the feather board. It features a https://abracon.com/realtimeclock/AB-RTCMC-32.768kHz-IBO5-S3.pdf RTC with a tiny superca for timekeeping. It will take care of generating the extcomin signal and minute-wise updates of the display. In between the updates the MCU can be turned off completely which can lead to very low  overall power consumption of the watch. That way one can just write Sketches for the nrf52840 without having to engineer low power stuff, so one should have a reliable device capable for everyday use. You have native USB for DFU und other communication via the charging cable which has a USB plug connected to the  four contacts anyway. The accelerometer is a BMA400 and the heart rate sensor based on https://pulsesensor.com sitting on a custom flex PCB connected to an analog input: https://github.com/BigCorvus/PulseSensor-for-SMA-Q2/tree/master

The current version snapfits almost perfectly into the LCD frame. Had to file a corner for a fraction of a millimeter.

The BOM is not quite finished yet because I have not setteled on the final component values, but most of them should be straightforward. Just consult the schematc. 
The dual P-Channel mosfets might be CMLDM8005 TR PBFREE (Digikey 1514-CMLDM8005TRPBFREECT-ND). 
Pushbuttons are LS12T2-T (Digikey 1642-1312-1-ND).
The supercap is Seiko CPH3225A (728-1127-1-ND). 
The RTC is Abracon AB-RTCMC-32.768kHz-IBO5-S3 (535-13301-1-ND). 
The display connectors are 255-3056-1-ND and 255-5667-ND. 
Accelerometer is 828-1081-1-ND (BMA400). 
Schottky diodes are 497-7163-1-ND. 
Flash chip is 1970-1011-1-ND. 
LDO is 296-24059-1-ND. 
The BT module is a Raytac MDBT50Q (1597-1678-ND). 
Watch crystal: 478-5428-1-ND. 
Mosfet for vibrator is DMG1012UW-7DICT-ND.
LED for HR sensor: 1497-1162-1-ND, Opamp: MCP6001T-I/LTCT-ND.
The vibration motor is 8mm in diameter and 2mm high. Can be found on Aliexpress.  
  
Newer version: https://github.com/BigCorvus/SMA-Q2_replacement_board_v2  
Arduino Firmware: 
 
