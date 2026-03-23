

```markdown
Register 7.46. LP_IO_GPIOn_REG (n: 0-7) (0x0048+0x4*n)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 15  | LP_GPIO_GPIOn_FUN_SEL                | Configures to select the LP IO MUX function for GPIO in normal execution mode. |
|     |                                     | 0: Select Function 0                                                         |
|     |                                     | 1: Select Function 1                                                         |
| ... |                                     | …                                                                             |
| (R/W)|                                     |                                                                                 |
| 14  | LP_GPIO_GPIOn_FUN_DRV               | Configures the drive strength of GPIO in normal execution mode.              |
|     |                                     | 0: ~5 mA                                                                     |
|     |                                     | 1: ~10 mA                                                                    |
|     |                                     | 2: ~20 mA                                                                    |
|     |                                     | 3: ~40 mA                                                                    |
| (R/W)|                                     |                                                                                 |
| 13  | LP_GPIO_GPIOn_FUN_IE                | Configures whether or not to enable the input of GPIO in normal execution mode.|
|     |                                     | 0: Not enable                                                                |
|     |                                     | 1: Enable                                                                    |
| (R/W)|                                     |                                                                                 |
| 12  | LP_GPIO_GPIOn_FUN_RUE               | Configures whether or not to enable the pull-up resistor of GPIO in normal execution mode.|
|     |                                     | 0: Not enable                                                                |
|     |                                     | 1: Enable                                                                    |
| (R/W)|                                     |                                                                                 |
| 11  | LP_GPIO_GPIOn_FUN_RDE               | Configures whether or not to enable the pull-down resistor of GPIO in normal execution mode.|
|     |                                     | 0: Not enable                                                                |
|     |                                     | 1: Enable                                                                    |
| (R/W)|                                     |                                                                                 |
| 10  | LP_GPIO_GPIOn_MCU_DRV               | Configures the drive strength of GPIO during sleep mode.                     |
|     |                                     | 0: ~5 mA                                                                     |
|     |                                     | 1: ~10 mA                                                                    |
|     |                                     | 2: ~20 mA                                                                    |
|     |                                     | 3: ~40 mA                                                                    |
| (R/W)|                                     |                                                                                 |

Continued on the next page...
```