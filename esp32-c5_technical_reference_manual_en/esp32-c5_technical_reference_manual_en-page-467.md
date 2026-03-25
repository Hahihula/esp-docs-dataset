

```markdown
EFUSE_ENABLE_SECURITY_DOWNLOAD

If this eFuse is 1, Joint Download Boot mode only allows reading, writing, and erasing plaintext flash and does not support any SRAM or register operations. Ignore this eFuse if Joint Download Boot mode is disabled.

EFUSE_DIS_DIRECT_BOOT

If this eFuse is 1, Direct Boot mode is disabled.
USB Serial/JTAG Controller can also force switch the chip to Joint Download Boot mode from SPI Boot mode, and vice versa. For detailed information, please refer to Chapter 37 USB Serial/JTAG Controller.

## 10.2.3 SDIO Sampling and Driving Clock Edge Control

The strapping pins GPIO25 and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table 10.2-3 SDIO Input Sampling Edge/Output Driving Edge Control.

Table 10.2-3. SDIO Input Sampling Edge/Output Driving Edge Control

| Edge behavior                                       | GPIO25 | MTDI |
|-----------------------------------------------------|--------|------|
| Falling edge sampling, falling edge output          | 0      | 0    |
| Falling edge sampling, rising edge output           | 0      | 1    |
| Rising edge sampling, falling edge output           | 1      | 0    |
| Rising edge sampling, rising edge output            | 1      | 1    |

¹ GPIO25 and MTDI are floating by default, so above are not default configurations.

## 10.2.4 ROM Messages Printing Control

During the boot process, the messages by the ROM code can be printed to:

*   (Default) UARTO and USB Serial/JTAG controller
    *   UARTO
    *   USB Serial/JTAG controller

To print ROM messages to UARTO or USB Serial/JTAG controller, see the description below.

EFUSE_UART_PRINT_CONTROL and GPIO27 control printing ROM messages to UARTO as shown in Table 10.2-4 UARTO ROM Message Printing Control.
```