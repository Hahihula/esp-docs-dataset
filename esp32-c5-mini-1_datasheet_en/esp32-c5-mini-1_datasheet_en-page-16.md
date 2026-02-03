**Title: Boot Configurations**

- **Subtitle:** USB Serial/JTAG controller

To print ROM messages to UART0 or USB Serial/JTAG controller, see the description below.

EFUSE_UART_PRINT_CONTROL and GPIO27 control printing ROM messages to UART0 as shown in Table 4-5.
UART0 ROM Message Printing Control...

**Table Title: Table 4-5. UART0 ROM Message Printing Control**

| **UART0 ROM Message Printing** | **Register^2** | eFuse^3 | GPIO27 |
| --- | --- | --- | --- |
| ROM messages are always printed to UART0 during boot | 0 (0b00) | x⁴ | - |
| Print is enabled during boot | 1 (0b01) | O | - |
| Print is disabled during boot | 2 (0b10) | O | - |
| Print is enabled during boot | 3 (0b11) | X | - |

**Footnotes:**
1. Bold marks the default value and configuration.
2. Register: LP_AON STORE4_REG[0]
3. eFuse: EFUSE_UART_PRINT_CONTROL
4. x: indicates that the value has no effect on the result and can be ignored.

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller as shown in Table 4-6 USB Serial/JTAG ROM Message Printing Control...

**Table Title: Table 4-6. USB Serial/JTAG ROM Message Printing Control**

| **USB Serial/JTAG ROM Message** | **EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT** |
| --- | --- |
| Printing | - |
| Enabled | O |
| Disabled | X |

**Footnotes for Table 4-6:**
1. Bold marks the default value and configuration.

**Title:** JTAG Signal Source Control

The strapping pin GPIO7 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.
As Table 4-7 shows, GPIO7 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE.

**Footer:**
Espressif Systems
ESP32-C5-MINI-1 Datasheet v1.0

[Submit Documentation Feedback](#)