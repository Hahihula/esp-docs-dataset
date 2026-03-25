

```markdown
Register 8.25. IO_MUX_GPIOn_REG (n: 0-14, 23-28) (0x0000+0x4*n)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 18  | IO_MUX_GPIOn_HYS_SEL                | Configures whether or not to enable the output of GPIO in sleep mode.        |
| 17  | IO_MUX_GPIOn_HYS_EN                 | O: Disable                                                                   |
|    |                                      | 1: Enable                                                                    |
| (R/W)|                                      |                                                                             |
| 16  | IO_MUX_GPIOn_FILTER_EN              | Configures whether or not to enter sleep mode for GPIO.                     |
| 15  |                                      | O: Not enter                                                                 |
|    |                                      | 1: Enter                                                                     |
| (R/W)|                                      |                                                                             |
| 14  | IO_MUX_GPIOn_MCU_OE                 | Configures whether or not to enable pull-down resistor of GPIO in sleep mode.|
| 13  |                                      | O: Disable                                                                   |
|    |                                      | 1: Enable                                                                    |
| (R/W)|                                      |                                                                             |
| 12  | IO_MUX_GPIOn_MCU_WPU                | Configures whether or not to enable pull-up resistor of GPIO during sleep mode.|
| 11  |                                      | O: Disable                                                                   |
|    |                                      | 1: Enable                                                                    |
| (R/W)|                                      |                                                                             |
| 10  | IO_MUX_GPIOn_MCU_IE                 | Configures whether or not to enable the input of GPIO during sleep mode.     |
| 9   |                                      | O: Disable                                                                   |
|    |                                      | 1: Enable                                                                    |
| (R/W)|                                      |                                                                             |
| 8   | IO_MUX_GPIOn_MCU_DRV                | Configures the drive strength of GPIO during sleep mode.                     |
| 7   |                                      | O: ~5 mA                                                                     |
|    |                                      | 1: ~10 mA                                                                    |
|    |                                      | 2: ~20 mA                                                                    |
|    |                                      | 3: ~40 mA                                                                    |
| (R/W)|                                      |                                                                             |
| 6   | IO_MUX_GPIOn_FUN_WPD                | Configures whether or not to enable pull-down resistor of GPIO.              |
| 5   |                                      | O: Disable                                                                   |
|    |                                      | 1: Enable                                                                    |
| (R/W)|                                      |                                                                             |
| 4-0 | Reset                                | All bits reset to 0x0                                                        |

Continued on the next page...
```