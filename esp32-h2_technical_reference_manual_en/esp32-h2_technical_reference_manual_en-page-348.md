

```markdown
- If this eFuse is 1, LP_AON_FORCE_DOWNLOAD_BOOT is disabled, and GPIO_STRAPPING can not be overwritten.

* EFUSE_DIS_DOWNLOAD_MODE

If this eFuse is 1, Joint Download Boot mode is disabled, and GPIO_STRAPPING will not be overwritten by LP_AON_FORCE_DOWNLOAD_BOOT.

* EFUSE_ENABLE_SECURITY_DOWNLOAD

If this eFuse is 1, Joint Download Boot mode only allows reading, writing, and erasing plaintext flash and does not support any SRAM or register operations. Ignore this eFuse if Joint Download Boot mode is disabled.

* EFUSE_DIS_DIRECT_BOOT

If this eFuse is 1, Direct Boot mode is disabled.
```

```markdown
USB Serial/JTAG Controller can also force switch the chip to Joint Download Boot mode from SPI Boot mode, and vice versa. For detailed information, please refer to Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG).
```

## 8.2.3 ROM Messages Printing Control

During the ROM boot stage of SPI Boot mode, GPIO8, LP_AON_STORE4_REG[0] and EFUSE_UART_PRINT_CONTROL jointly control the printing of ROM messages.

Table 8.2-3. ROM Message Printing Control

| Register¹ | eFuse² | GPIO8   | ROM Message Printing                                                                 |
|-----------|--------|---------|---------------------------------------------------------------------------------------|
|           |        | x³      | ROM messages are always printed to UART0 during boot                                 |
|           |        | (Ob00)  |                                                                                        |
| O         | 1 (Ob01)| 0       | Print is enabled during boot                                                         |
|           |        | 1       | Print is disabled during boot                                                       |
|           | 2 (Ob10)| 0       | Print is disabled during boot                                                       |
|           |        | 1       | Print is enabled during boot                                                       |
|           | 3 (Ob11)| x       | Print is disabled during boot                                                       |
| 1         | x      | x       | Print is disabled during boot                                                       |

¹ Register: LP_AON_STORE4_REG[0]
² eFuse: EFUSE_UART_PRINT_CONTROL
³ x: values that have no effect on the result and can therefore be ignored.

ROM message is printed to UART0 and USB Serial/JTAG Controller by default during power-on. Users can disable the printing to USB Serial/JTAG Controller by setting the eFuse bit EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT.

Note that if EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT is set to 0 to print to USB, but the USB Serial/JTAG Controller has been disabled, then ROM messages will not be printed to USB Serial/JTAG Controller.
```