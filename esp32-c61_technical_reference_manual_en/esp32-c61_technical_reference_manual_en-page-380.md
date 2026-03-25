

```markdown
Register 7.64. LP_CLKRST_LP_CLK_PO_EN_REG (0x0004)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 11  | LP_CLKRST_LP_BUS_OEN                 | Configures whether to gate the LP_DYN_SLOW_CLK signals to pad.               |
| 10  | LP_CLKRST_RNG_OEN                    | Enables clock gate                                                            |
| 9   | LP_CLKRST_FAST_OEN                   |                                                                             |
| 8   | LP_CLKRST_SLOW_OEN                   |                                                                             |
| 7   | LP_CLKRST_CORE_OEN                   |                                                                             |
| 6   | LP_CLKRST_XTAL32K_OEN                |                                                                             |
| 5   | (reserved)                           |                                                                             |
| 4   | LP_CLKRST_FOSC_OEN                   |                                                                             |
| 3   | LP_CLKRST_SOSC_OEN                   |                                                                             |
| 2   | LP_CLKRST_AON_SLOW_OEN               | Configures whether to gate the LP_DYN_SLOW_CLK signals to pad.               |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
| 1   | LP_CLKRST_AON_FAST_OEN               | Configures whether to gate the LP_DYN_FAST_CLK signals to pad.               |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
| 0   | LP_CLKRST_SLOW_OEN                   | Configures whether to gate the OSC_SLOW_CLK signals to pad.                  |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
|     | LP_CLKRST_FOSC_OEN                   | Configures whether to gate the RC_FAST_CLK signals to pad.                   |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
|     | LP_CLKRST_XTAL32K_OEN                | Configures whether to gate the XTAL32K_CLK signals to pad.                   |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
|     | LP_CLKRST_CORE_EFUSE_OEN             | Configures whether to gate the EFUSE_CTRL clock.                             |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
|     | LP_CLKRST_SLOW_OEN                   | Configures whether to gate the LP_SLOW_CLK signals to pad.                   |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |
|     | LP_CLKRST_FAST_OEN                   | Configures whether to gate the LP_FAST_CLK signals to pad.                   |
|     |                                     | 0: Disable the clock gate<br>1: Enable the clock gate (R/W)                  |

Continued on the next page...
```