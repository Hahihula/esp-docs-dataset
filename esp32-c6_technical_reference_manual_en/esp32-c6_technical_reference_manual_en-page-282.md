

```markdown
Register 7.20. IO_MUX_GPIOn_REG (n: 0-30) (0x0004+4*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 15  | IO_MUX_GPIOn_FILTER_EN        | Configures whether or not to enable the output of GPIO in sleep mode.       |
|     |                                | 0: Disable<br>1: Enable (R/W)                                               |
| 14  | IO_MUX_GPIOn_MCU_OE           | Configures whether or not to enter sleep mode for GPIO.<br>0: Not enter<br>1: Enter (R/W) |
| 13  | IO_MUX_GPIOn_MCU_WPD          | Configure whether or not to enable pull-down resistor of GPIO in sleep mode.<br>0: Disable<br>1: Enable (R/W) |
| 12  | IO_MUX_GPIOn_MCU_WPDU         | Configures whether or not to enable pull-up resistor of GPIO during sleep mode.<br>0: Disable<br>1: Enable (R/W) |
| 11  | IO_MUX_GPIOn_MCU_IE           | Configures whether or not to enable the input of GPIO during sleep mode.<br>0: Disable<br>1: Enable (R/W) |
| 10  | IO_MUX_GPIOn_MCU_DRV          | Configures the drive strength of GPIO during sleep mode.<br>0: ~5 mA<br>1: ~10 mA<br>2: ~20 mA<br>3: ~40 mA (R/W) |
| 9   | IO_MUX_GPIOn_FUN_WPD          | Configures whether or not to enable pull-down resistor of GPIO.<br>0: Disable<br>1: Enable (R/W) |

Continued on the next page...
```