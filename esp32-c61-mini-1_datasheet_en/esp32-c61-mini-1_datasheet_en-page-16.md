Title: Boot Configurations

Body Text:
- In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.
- In Joint Download Boot mode, users can download binary files into flash using UARTO, USB or SDIO Slave interfaces and execute it in SPI Boot mode.

Subtitle: 4.2 SDIO Sampling and Driving Clock Edge Control

Body Text:
The strapping pin MTMS and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table 8 SDIO Input Sampling Edge/Output Driving Edge Control.

Table Title: Table 8: SDIO Input Sampling Edge/Output Driving Edge Control
- Column Headers: Edge behavior, MTMS, MTDI
- Rows:
  - Falling edge sampling, falling edge output | 0 | 0
  - Rising edge sampling, rising edge output | 1 | 1

Footnote for Table 8 (indicated by superscript numbers):
1. MTMS and MTDI are floating by default; so above are not default configurations.

Subtitle: 4.3 ROM Messages Printing Control

Body Text:
During the boot process, the messages by the ROM code can be printed to:

- (Default) UARTO and USB Serial/JTAG controller
- USB Serial/JTAG controller
- UARTO

List of registers with their descriptions for printing control from LP_AON_STORE4_REG[0], EFUSE_UART_PRINT_CONTROL, and GPIO8:
- LP_AON_STORE4_REG[0] | EFUSE_UART_PRINT_CONTROL | GPIO8 (as shown in Table 9 UARTO ROM Message Printing Control)

Table Title: Table 9: UARTO ROM Message Printing Control
- Column Headers: UARTO ROM Code Printing, EFUSE_UART_PRINT_CONTROL, GPIO8 Register
- Rows:
  - Always enabled^2 | 0 | Ignored
    - Enabled | 1 | O
    - Disabled | 1 | 1
    - Disabled | 2 | 0

Footnote for Table 9 (indicated by superscript numbers):
1. Register: LP_AON_STORE4_REG[0]
2. Bold marks the default value and configuration.

Footer:
- Espresso Systems, Page number "16", Document version "ESP32-C61-MINI-I & MINI-1U Datasheet v0.6"
- Submit Documentation Feedback