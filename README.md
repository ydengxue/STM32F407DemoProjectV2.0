# Demo for STM32F407
Author: **[Dengxue Yan](https://sites.google.com/site/ydengxue/)**
****

This is a DEMO project for a simple single-task system on STM32F407:
1. Boot.bin is for BOOTing the user Application. It supports XMODEM download mode. The downloaded file must be handled by File2Bin.exe first and will be place at address 0x08020000.Debug UART uses UART 0 - 115200,8,n,1.
2. User Application need to be located at Address 0x08020000(The address of starting isr vectors)
3. The DEMO user project:
    a. Debug UART uses UART 0 - 115200,8,n,1.
    b. Communication UARTs are UART 2 and UART 4(Suport modbus at present).
    c. External 1M memory is at address 0x68000000 which is FSMC bank 1 NOR/PSRAM 3
    d. SPI flash localte at SPI1
    d. Support Devcfg.bin download and parse

Since some code is packed in the libs, if you are interested in this system, please send me email at dengxue.yan@wustl.edu
