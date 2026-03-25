
```markdown
Table 10.2-4. UARTO ROM Message Printing Control

| UARTO ROM Message Printing | Register² | eFuse³ | GPIO27 |
|----------------------------|-----------|---------|--------|
| ROM messages are always printed to UARTO during boot |           |         |        |
| Print is enabled during boot |           | 0 (Ob00) | x⁴     |
| Print is disabled during boot |           | 1 (Ob01) | O      |
| Print is disabled during boot | O         | 2 (Ob10) | 0      |
| Print is enabled during boot |           | 3 (Ob11) | x      |
| Print is disabled during boot | 1         | x       | x      |

¹ Bold marks the default value and configuration.
² Register: LP_AON_STORE4_REG[0]
³ eFuse: EFUSE_UART_PRINT_CONTROL
⁴ x: x indicates that the value has no effect on the result and can be ignored.

EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT controls the printing to USB Serial/JTAG controller as shown in Table 10.2-5 USB Serial/JTAG ROM Message Printing Control.

Table 10.2-5. USB Serial/JTAG ROM Message Printing Control

| USB Serial/JTAG<br>ROM Message<br>Printing | EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT |
|--------------------------------------------|-------------------------------------|
| Enabled                                    | 0                                   |
| Disabled                                   | 1                                   |
|                                            | Ignored                             |

¹ Bold marks the default value and configuration.

10.2.5 JTAG Signal Source Control

The strapping pin GPIO7 can be used to control the JTAG signal source during the early boot process. This pin does not have internal pull-up or pull-down resistors, so its strapping value must be controlled by an external circuit that must not be in a high-impedance state.

GPIO7 controls the source of JTAG signals together with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG and EFUSE_JTAG_SEL_ENABLE. See Table 10.2-6 JTAG Signal Source Control.
```