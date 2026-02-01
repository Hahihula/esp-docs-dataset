Title: Boot Configurations

Subtitle: In Joint Download Boot mode, it is also possible to download binary files into SRAM using UARTO, USB or SDIO Slave interfaces and execute it from SRAM.

Section Title: 3.2 SDIO Sampling and Driving Clock Edge Control

Body Text:
The strapping pin MTMS and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table 3-4 SDIO Input Sampling Edge/Output Driving Edge Control.

Table Caption (Table Title): Table 3-4: SDIO Input Sampling Edge/Output Driving Edge Control

Table:
| Edge behavior | MTMS | MTDI |
|----------------|------|------|
| Falling edge sampling, falling edge output | 0 | 0 |
| Falling edge sampling, rising edge output | 0 | 1 |
| Rising edge sampling, falling edge output | 1 | 0 |
| Rising edge sampling, rising edge output | 1 | 1 |

Footnote:
¹ MTMS and MTDI are floating by default, so above are not default configurations.

Section Title: 3.3 ROM Messages Printing Control

Body Text:
During the boot process, the messages by the ROM code can be printed to:

- (Default) UARTO and USB Serial/JTAG controller
- USB Serial/JTAG controller
- UARTO

LP_AON_STORE4_REG[0], EFUSE_UART_PRINT_CONTROL and GPIO8 control ROM messages printing to UARTO as shown in Table 3-5 UARTO ROM Message Printing Control.

Table Caption: Table 3-5: UARTO ROM Message Printing Control

Table:
| UARTO ROM Code Printing | EFUSE_UART_PRINTControl | GPIO8 Register |
|-------------------------|--------------------------|----------------|
| Always enabled²        | 0                        | Ignored        |
| Enabled                 | 1                        | 0              |
| Disabled                | 2                        | 0              |
| Enabled                 | 3                        | Ignored        |
| Always disabled         |                         |               |

Footnotes:
¹ Register: LP_AON_STORE4_REG[0]
² Bold marks the default value and configuration.

Body Text (continued):
EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT and LP_AON_STORE4_REG[0] control the printing to USB Serial/JTAG controller as shown in Table 3-6 USB Serial/JTAG ROM Message Printing Control.

Footer:
Espressif Systems
29 ESP32-C61 Series Datasheet v0.5