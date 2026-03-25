

```markdown
Register 6.55. LP_IO_MUX_GPIO{n}_REG (n: 0-6) (0x0000+0x4*n)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | LP_IO_MUX_GPIO{n}_HYS_SEL                 | Configures the hysteresis level of GPIO{n}.                                 |
| 29  | LP_IO_MUX_GPIO{n}_FILTER_EN               | Enables/disables filter for GPIO{n} input.                                  |
| 28  | LP_IO_MUX_GPIO{n}_SEL                     | Selects function for GPIO{n}.                                                |
| 27  | LP_IO_MUX_GPIO{n}_MCU_OE                  | Configures whether or not to enable the output of GPIO{n} during sleep mode.<br>0: Not enable<br>1: Enable (R/W) |
| 26  | LP_IO_MUX_GPIO{n}_SLP_SEL                 | Configures whether or not to enable the sleep mode for GPIO{n}.<br>0: Not enable<br>1: Enable (R/W) |
| 25  | LP_IO_MUX_GPIO{n}_MCU_WPD                 | Configures whether or not to enable the pull-down resistor of GPIO{n} during sleep mode.<br>0: Not enable<br>1: Enable (R/W) |
| 24  | LP_IO_MUX_GPIO{n}_MCU_WPU                 | Configures whether or not to enable the pull-up resistor of GPIO{n} during sleep mode.<br>0: Not enable<br>1: Enable (R/W) |
| 23  | LP_IO_MUX_GPIO{n}_MCU_IE                  | Configures whether or not to enable the input of GPIO{n} during sleep mode.<br>0: Not enable<br>1: Enable (R/W) |
| 22  | LP_IO_MUX_GPIO{n}_MCU_DRV                 | Configures the drive strength of GPIO{n} during sleep mode.<br>0: ~5 mA<br>1: ~10 mA<br>2: ~20 mA<br>3: ~40 mA (R/W) |
| 21-16| LP_IO_MUX_GPIO{n}_FUN_DRV                 |                                                                             |
| 15  | LP_IO_MUX_GPIO{n}_FUN_IE                  |                                                                             |
| 14  | LP_IO_MUX_GPIO{n}_FUN_WPU                 |                                                                             |
| 13  | LP_IO_MUX_GPIO{n}_MCU_DRV                 |                                                                             |
| 12  | LP_IO_MUX_GPIO{n}_WPD                     |                                                                             |
| 11  | LP_IO_MUX_GPIO{n}_SEL                     |                                                                             |
| 10  | LP_IO_MUX_GPIO{n}_OE                      |                                                                             |
| 9   | LP_IO_MUX_GPIO{n}_MCU_OE                  |                                                                             |
| 8-0 | Reset                                     | 0x000 (Reset value)                                                           |

Continued on the next page...
```