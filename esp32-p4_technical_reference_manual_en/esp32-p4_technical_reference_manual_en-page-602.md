

```markdown
Register 9.43. IO_MUX_GPIOn_REG (n: 0 - 54) (0x0004+4*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 16  | IO_MUX_GPIOn_FILTER_EN        |                                                                             |
| 15  | IO_MUX_GPIOn_MCU_SEL          |                                                                             |
| 14  | IO_MUX_GPIOn_FUN_DRV          |                                                                             |
| 13  | IO_MUX_GPIOn_FUN_IE           |                                                                             |
| 12  | IO_MUX_GPIOn_MCU_WPU          |                                                                             |
| 11  | IO_MUX_GPIOn_MCU_WPDU         |                                                                             |
| 10  | IO_MUX_GPIOn_SLP_SEL          |                                                                             |
| 9   | IO_MUX_GPIOn_MCU_IE           |                                                                             |
| 8   | IO_MUX_GPIOn_MCU_DRV          |                                                                             |
| 7-3 | reserved                      |                                                                             |
| 2   | IO_MUX_GPIOn_MCU_OE           | Configures whether or not to enable the output of GPIOn in sleep mode.       |
|     | O: Disable                    |                                                                                 |
|     | 1: Enable                    | (R/W)                                                                         |
| 1   | IO_MUX_GPIOn_SLP_SEL          | Configures whether or not to enter sleep mode for GPIOn.                   |
|     | O: Not enter                 |                                                                                 |
|     | 1: Enter                     | (R/W)                                                                         |
| 0   | IO_MUX_GPIOn_MCU_WPU          | Configure whether or not to enable pull-up resistor of GPIOn during       |
|     | sleep mode.                  |                                                                                 |
|     | O: Disable                   |                                                                                 |
|     | 1: Enable                    | (R/W)                                                                         |
|     | IO_MUX_GPIOn_MCU_WPDU         | Configures whether or not to enable pull-down resistor of GPIOn during   |
|     | sleep mode.                  |                                                                                 |
|     | O: Disable                   |                                                                                 |
|     | 1: Enable                    | (R/W)                                                                         |
|     | IO_MUX_GPIOn_MCU_IE           | Configures whether or not to enable the input of GPIOn during sleep       |
|     | mode.                        |                                                                                 |
|     | O: Disable                   |                                                                                 |
|     | 1: Enable                    | (R/W)                                                                         |
|     | IO_MUX_GPIOn_MCU_DRV          | Configures the drive strength of GPIOn during sleep mode.                  |
|     | O: ~5 mA                     |                                                                                 |
|     | 1: ~10 mA                    |                                                                                 |
|     | 2: ~20 mA                    |                                                                                 |
|     | 3: ~40 mA                    | (R/W)                                                                         |

Continued on the next page...
```