

```markdown
Boot mode by setting register LPSYSREG_FORCE_DOWNLOAD_BOOT and triggering a CPU reset. If this eFuse is 1, LPSYSREG_FORCE_DOWNLOAD_BOOT is disabled.

*   **EFUSE_DIS_DOWNLOAD_MODE**
    If this eFuse is 1, Joint Download Boot mode is permanently disabled.
*   **EFUSE_ENABLE_SECURITY_DOWNLOAD**
    If this eFuse is 1, Joint Download Boot mode only allows reading, writing, and erasing plaintext flash and does not support any L2MEM or register operations. Ignore this eFuse if Download Boot mode is disabled.
*   **EFUSE_DIS_DIRECT_BOOT**

If this eFuse is 1, Direct Boot would be disabled in SPI Boot Mode.

USB Serial/JTAG Controller can also force switch the chip to Joint Download Boot mode from SPI Boot mode, and vice versa. For detailed information, please refer to Chapter 51 USB Serial/JTAG Controller (USB_SERIAL_JTAG).

You can set eFuse bit EFUSE_DIS_USB_SERIAL_JTAG_DOWNLOAD_MODE to disable USB Serial/JTAG Controller from force switching to Joint Download Boot mode.

## 11.2.3 ROM Messages Printing Control

During early SPI Boot process, the messages by the ROM code can be printed to:

*   (Default) UARTO and USB Serial/JTAG controller
*   UARTO
*   USB Serial/JTAG controller

EFUSE_UART_PRINT_CONTROL and GPIO36 control ROM messages printing to UARTO as shown in Table 11.2-3 ROM Message Printing Control.

Table 11.2-3. ROM Message Printing Control

| eFuse¹ | GPIO36 | ROM Code Printing |
|--------|--------|-------------------|
| 0      | x²     | Always enabled    |
|        | 0      | Enabled           |
|        | 1      | Disabled          |
| 2      | 0      | Disabled          |
|        | 1      | Enabled           |
| 3      | x      | Always disabled   |

¹ eFuse: EFUSE_UART_PRINT_CONTROL
² x: values that have no effect on the result and can therefore be ignored.

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller. When this bit is 1, printing to USB Serial/JTAG controller is disabled. When this bit is 0, and USB Serial/JTAG controller is enabled via EFUSE_DIS_USB_SERIAL_JTAG, ROM messages can be printed to USB Serial/JTAG controller.
```