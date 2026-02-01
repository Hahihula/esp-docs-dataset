Title: Boot Configurations

Body Text:
In Joint Download Boot mode, users can download binary files into flash using UARTO or USB interface. It is also possible to download binary files into SRAM and execute it from SRAM.

In addition to SPI Boot and Joint Download Boot modes, ESP32-C3 also supports SPI Download Boot mode.
For details, please see [ESP32-C3 Technical Reference Manual > Chapter Chip Boot Control](#).

Subtitle: 4.2 ROM Messages Printing Control

Body Text:
During the boot process, the messages by the ROM code can be printed to:

- (Default) UARTO and USB Serial/JTAG controller
- UARTO
- USB Serial/JTAG controller

EFUSE_UART_PRINT_CONTROL and GPIO8 control ROM messages printing to UARTO as shown in Table 4-4.

Table Title: UARO ROM Message Printing Control

Table:
| UARTO ROM Code Printing | EFUSE_UART_PRINT_CONTROL | GPIO8 |
|-------------------------|----------------------------|-------|
|                        | 0                          | Ignored |
| Enabled                | 1                          | 0     |
|                        | 2                          | 1     |
| Disabled               | 1                          | 1     |
|                        | 2                          | 0     |
|                        | 3                          | Ignored |

Body Text:
EFUSE_USB_PRINT_CHANNEL controls the printing to USB Serial/JTAG controller as shown in Table 4-5 USB Serial/JTAG ROM Message Printing Control.

Table Title: Table 4-5. USB Serial/JTAG ROM Message Printing Control

Table:
| USB Serial/JTAG | EFUSE_DIS_USB_SERIAL_JTAG | EFUSE_USB_PRINT_CHANNEL |
|------------------|----------------------------|-------------------------|
|                  |                            |                        |
| Enabled          | 0                          | 0                       |
| Disabled         | 0                          | 1                       |
|                  | 1                          | Ignored                 |

Body Text:
EFUSE_DIS_USB_SERIAL_JTAG controls whether to disable USB Serial/JTAG.

Subtitle: 4.3 Chip Power-up and Reset

Body Text:
Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_EN – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_EN as well as power-up and reset timing, see Figure 4-2 and Table 4-6.

Footer:
Espressif Systems
Page Number: 14

Link Texts/References in Body Text (Hyperlinks):
[ESP32-C3 Technical Reference Manual > Chapter Chip Boot Control](#)

Document Footer Links:
Submit Documentation Feedback