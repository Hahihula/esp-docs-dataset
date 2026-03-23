

```markdown
If this eFuse is 1, Download Boot mode is permanently disabled. GPIO_STRAPPING will not be overwritten by LP_AON_FORCE_DOWNLOAD_BOOT.

*   EFUSE_ENABLE_SECURITY_DOWNLOAD

    If this eFuse is 1, Download Boot mode only allows reading, writing, and erasing plaintext flash and does not support any SRAM or register operations. Ignore this eFuse if Download Boot mode is disabled.

*   EFUSE_DIS_DIRECT_BOOT

    If this eFuse is 1, Direct Boot mode is disabled.
    
USB Serial/JTAG Controller can also force switch the chip to Download Boot mode from SPI Boot mode, and vice versa. For detailed information, please refer to Chapter 32 USB Serial/JTAG Controller (USB_SERIAL_JTAG).

## 9.2.3 ROM Messages Printing Control

During early SPI Boot process the messages by the ROM code can be printed to:

*   (Default) UARTO and USB Serial/JTAG controller
*   USB Serial/JTAG controller
*   UARTO

EFUSE_UART_PRINT_CONTROL and GPIO8 control ROM messages printing to UARTO as shown in Table 9.2-3 ROM Message Printing Control.

Table 9.2-3. ROM Message Printing Control

| eFuse¹ | GPIO8 | ROM Code Printing |
|--------|-------|-------------------|
| 0      | x     | Always enabled    |
|        | O     | Enabled           |
| 1      | 1     | Disabled          |
| 2      | O     | Disabled          |
|        | 1     | Enabled           |
| 3      | x     | Always disabled   |

¹ eFuse: EFUSE_UART_PRINT_CONTROL

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller. When this bit is 1, printing to USB Serial/JTAG controller is disabled. When this bit is 0, and USB Serial/JTAG controller is enabled via EFUSE_DIS_USB_SERIAL_JTAG, ROM messages can be printed to USB Serial/JTAG controller.

Note that if EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT is set to 0 to print to USB, but USB Serial/JTAG Controller has been disabled, then ROM messages will not be printed to USB Serial/JTAG Controller.

## 9.2.4 JTAG Signal Source Control

GPIO15 controls the source of JTAG signals during the early boot process. This GPIO is used together with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE. See Table 9.2-4.
```