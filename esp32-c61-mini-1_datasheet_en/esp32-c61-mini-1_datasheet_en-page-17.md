Title: Boot Configurations

Body Text:
EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT and LP_AON_STORE4_REG[0] control the printing to USB Serial/JTAG controller as shown in Table 10 USB Serial/JTAG ROM Message Printing Control.

Table Title (with headers): Table 10: USB Serial/JTAG ROM Message Printing Control

| USB Serial/JTAG ROM Message | LP_AON_STORE4_REG[0] | EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT |
|------------------------------|-----------------------|--------------------------------------|
| Printing Control             |                       |                                      |
| Enabled                      | 0                     | 0                                    |
| Disabled                     | 1                     | Ignored                              |

Note: "Bold marks the default value and configuration."

Subtitle: JTAG Signal Source Control

Body Text:
The strapping pin GPIO7 can be used to control the source of JTAG signals during the early boot process. This pin does not have any internal pull resistors and the strapping value must be controlled by the external circuit that cannot be in a high impedance state.

As Table 11 shows, GPIO7 is used in combination with EFUSE_DIS_PAD_JTAG, EFUSE_DIS_USB_JTAG, and EFUSE_JTAG_SEL_ENABLE.

Table Title (with headers): Table 11: JTAG Signal Source Control

| eFuse | eFuse | eFuse | GPIO7 | JTAG Signal Source |
|-------|-------|-------|-------|--------------------|
|       | 2^2   | 3^3   | x4    | USB Serial/JTAG Controller |
| 0     | O     | 0     |        |                      |
| 0     | X     | X     |        | JTAG pins MTDI, MTCK, MTMS and MTDO |
| 1     |       |       |       | USB Serial/JTAG Controller |
| 1     |       |       |       | JTAG is disabled |

Footnotes:
1. eFuse: EFUSE_DIS_PAD_JTAG
2. eFuse: EFUSE_DIS_USB_JTAG
3. eFuse: EFUSE_JTAG_SEL_ENABLE

Note at the bottom of the table (for GPIO7): x indicates that the value has no effect on the result and can be ignored.

Note 5 in Table Title:
Bold marks the default value and configuration.

Footer Text:
Espressif Systems
17 ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

Link: Submit Documentation Feedback