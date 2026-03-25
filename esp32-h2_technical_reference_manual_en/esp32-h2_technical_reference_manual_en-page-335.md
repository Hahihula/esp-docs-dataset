

```markdown
Chapter 7 Reset and Clock

Register 7.78. LP_CLKRST_LP_CLK_PO_EN_REG (0x0004)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 11-9| LP_CLKRST_LP_BUS_OEN, LP_CLKRST_RNG_OEN, LP_CLKRST_FAST_OEN |
| 8   | LP_CLKRST_SLOW_OEN |
| 7   | LP_CLKRST_CORE_SLOW_OEN |
| 6   | (reserved) |
| 5   | LP_CLKRST_XTAL32K_OEN |
| 4   | LP_CLKRST_FOSC_OEN |
| 3   | LP_CLKRST_AON_SLOW_OEN |
| 2   | LP_CLKRST_SOSC_OEN |
| 1   | LP_CLKRST_FAST_OEN |
| 0   | Reset |

LP_CLKRST_AON_SLOW_OEN Configures whether to gate the LP_DYN_SLOW_CLK signals to pad.
- 0: Disable the clock gate
- 1: Enable the clock gate
(R/W)

LP_CLKRST_AON_FAST_OEN Configures whether to gate the LP_DYN_FAST_CLK signals to pad.
- 0: Disable the clock gate
- 1: Enable the clock gate
(R/W)

LP_CLKRST_SOSC_OEN Configures whether to gate the OSC_SLOW_CLK signals to pad.
- 0: Disable the clock gate
- 1: Enable the clock gate
(R/W)

LP_CLKRST_FOSC_OEN Configures whether to gate the RC_FAST_CLK signals to pad.
- 0: Disable the clock gate
- 1: Enable the clock gate
(R/W)

LP_CLKRST_XTAL32K_OEN Configures whether to gate the XTAL32K_CLK signals to pad.
- 0: Disable the clock gate
- 1: Enable the clock gate
(R/W)

Continued on the next page...
```