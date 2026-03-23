

```markdown
- If this eFuse is 1, `RTC_CNTL_FORCE_DOWNLOAD_BOOT` is disabled. `GPIO_STRAPPING` can not be overwritten.

* EFUSE_DIS_DOWNLOAD_MODE

If this eFuse is 1, Joint Download Boot mode is disabled. `GPIO_STRAPPING` will not be overwritten by `RTC_CNTL_FORCE_DOWNLOAD_BOOT`.

* EFUSE_ENABLE_SECURITY_DOWNLOAD

If this eFuse is 1, Joint Download Boot mode only allows reading, writing, and erasing plaintext flash and does not support any SRAM or register operations. Ignore this eFuse if Joint Download Boot mode is disabled.

* EFUSE_DIS_DIRECT_BOOT

If this eFuse is 1, Direct Boot mode is disabled.

USB Serial/JTAG Controller can also force the chip into Joint Download Boot mode from SPI Boot mode, as well as force the chip into SPI Boot mode from Joint Download Boot mode. For detailed information, please refer to Chapter 30 USB Serial/JTAG Controller (USB_SERIAL_JTAG).

## 7.3 ROM Messages Printing Control

During early SPI Boot process, the messages by the ROM code can be printed to:

* (Default) UARTO and USB Serial/JTAG controller
* UARTO
* USB Serial/JTAG controller

`EFUSE_UART_PRINT_CONTROL` and GPIO8 control ROM messages printing to UARTO as shown in Table 7.3-1.

Table 7.3-1. ROM Message Printing Control

| eFuse¹ | GPIO8 | ROM Code Printing                                                                 |
|--------|-------|-------------------------------------------------------------------------------------|
| 0      | x     | ROM code is always printed to UARTO during boot. The value of GPIO8 is ignored.    |
| 1      | 0     | Print is enabled during boot.                                                      |
|        | 1     | Print is disabled during boot.                                                     |
| 2      | 0     | Print is disabled during boot.                                                     |
|        | 1     | Print is enabled during boot.                                                      |
| 3      | x     | Print is always disabled during boot. The value of GPIO8 is ignored.               |

¹ eFuse: `EFUSE_UART_PRINT_CONTROL`

`EFUSE_USB_PRINT_CHANNEL` controls the printing to USB Serial/JTAG controller. When this bit is 1, printing to USB Serial/JTAG controller is disabled. When this bit is 0 and the USB Serial/JTAG controller is enabled via `EFUSE_DIS_USB_SERIAL_JTAG`, ROM messages can be printed to USB Serial/JTAG controller.
```