# Turbosound AVR AY Emul v1.0

TurboSound Emulator on 2x Atmega8A chips based on http://www.avray.ru project.

![image](https://github.com/andykarpov/turbosound28p/raw/master/docs/turbosound28p_photo_back.jpg)
![image](https://github.com/andykarpov/turbosound28p/raw/master/docs/turbosound28p_photo_front.jpg)

## How to upload the firmware
Due to there is no room for ISP connectors on the board, you need to solder a few wires directly on the board and connect them with your programmer:
- GND, VCC and RESET signals 
- CK, SO, SI as SCLK, MISO and MOSI signals 
- Do not forget to bridge solder jumpers

### Uploading:

Use avrdude and USBAsp programmer to upload firmware for each chip:

avrdude -p atmega8 -c USBasp -U flash:w:emul_230_turbosound_chip0.hex -U eeprom:w:Conf_parallel_24MHz_1_75Mhz.hex -U lfuse:w:0xCE:m -U hfuse:w:0xCF:m
avrdude -p atmega8 -c USBasp -U flash:w:emul_230_turbosound_chip1.hex -U eeprom:w:Conf_parallel_24MHz_1_75Mhz.hex -U lfuse:w:0xCE:m -U hfuse:w:0xCF:m

