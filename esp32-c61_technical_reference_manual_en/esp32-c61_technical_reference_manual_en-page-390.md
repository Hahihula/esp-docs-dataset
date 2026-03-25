
```markdown
| LP_AON_STORE4_REG[0] | EFUSE_UART_PRINT_CONTROL | GPIO8 | ROM Message Printing |
|----------------------|--------------------------|-------|----------------------|
|                      |                          | x¹    | Always printed to UARTO |
| 0                    | 0 (Ob00)                 |       |                      |
|                      |                          | 0     | Enabled              |
|                      | 1 (Ob01)                 | 1     | Disabled             |
| O                    |                          | O     | Disabled             |
|                      | 2 (Ob10)                 | 1     | Enabled              |
|                      | 3 (Ob11)                 | x     | Disabled             |
| 1                    | x                        | x     | Disabled             |

¹ x: values that have no effect on the result and can therefore be ignored.
```

ROM message is printed to UARTO and USB Serial/JTAG Controller by default during power-on. Users can disable the printing to USB Serial/JTAG Controller by setting the eFuse bit EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT.

Note that if EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT is set to 0 to print to USB, but the USB Serial/JTAG Controller has been disabled, then ROM messages will not be printed to USB Serial/JTAG Controller.

## 8.2.5 JTAG Signal Source Control

The strapping pin GPIO7 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 8.2-5 shows, GPIO7 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE.

```markdown
| EFUSE_DIS_PAD_JTAG | EFUSE_DIS_USB_JTAG | EFUSE_JTAG_SEL_ENABLE | GPIO7 | JTAG Signal Source |
|--------------------|--------------------|------------------------|-------|--------------------|
|                    |                    |                        | x¹    | USB Serial/JTAG Controller |
| 0                  | 0                  | 1                      | 1     |                    |
|                    | O                  |                        |       |                    |
| 0                  | x                  | x                      | x     | JTAG pins MTDI, MTCK, MTMS, and MTDO |
| 0                  | 1                  | x                      | x     |                    |
| 1                  | 0                  | x                      | x     | USB Serial/JTAG Controller |
| 1                  | 1                  | x                      | x     | JTAG is disabled   |

¹ x: x indicates that the value has no effect on the result and can be ignored.
```