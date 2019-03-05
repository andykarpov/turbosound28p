TurboSound Emulator

Based on
AVR Emulator of IC AY-8910, AY-3-8910, AY-3-8912 for Atmega8,Atmega8A
Version 23.0 with speaker support (19.02.2016) Parallel mode only!
HI-Z read mode version

Uploading:

	Use avrdude and USBAsp programmer:

        avrdude -p atmega8 -c USBasp -U flash:w:emul_230_turbosound_chip0.hex -U eeprom:w:Conf_parallel_24MHz_1_75Mhz.hex -U lfuse:w:0xCE:m -U hfuse:w:0xCF:m
        avrdude -p atmega8 -c USBasp -U flash:w:emul_230_turbosound_chip1.hex -U eeprom:w:Conf_parallel_24MHz_1_75Mhz.hex -U lfuse:w:0xCE:m -U hfuse:w:0xCF:m

files emul_230_turbosound_chip0.hex - Firmware for chip 0
files emul_230_turbosound_chip1.hex - Firmware for chip 1

ORIGIN: http://www.avray.ru
