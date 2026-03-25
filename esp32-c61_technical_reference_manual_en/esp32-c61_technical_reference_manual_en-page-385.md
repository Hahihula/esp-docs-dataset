

```markdown
Chapter 7 Reset and Clock

Register 7.70. LP_CLKRST_CLK_TO_HP_REG (0x0020)

| Bit | Description |
|-----|-------------|
| 31  | LP_CLKRST_ICG_HP_FOSC reserved |
| 30  | LP_CLKRST_ICG_HP_SOSC |
| 29  | LP_CLKRST_ICG_HP_XTAL32K |

LP_CLKRST_ICG_HP_FOSC Configures whether to gate the RC_FAST_CLK signals to HP system.
- O: Disable the clock gate
- 1: Enable the clock gate (R/W)

LP_CLKRST_ICG_HP_SOSC Configures whether to gate the RC_SLOW_CLK signals to HP system.
- O: Disable the clock gate
- 1: Enable the clock gate (R/W)

LP_CLKRST_ICG_HP_XTAL32K Configures whether to gate the XTAL32K_CLK signals to HP system.
- O: Disable the clock gate
- 1: Enable the clock gate (R/W)

Register 7.71. LP_CLKRST_DATE_REG (0x03FC)

| Bit | Description |
|-----|-------------|
| 31  | LP_CLKRST_CLK_EN |
| 30  | LP_CLKRST_CLKRST_DATE |

LP_CLKRST_CLKRST_DATE Version control register. (R/W)

LP_CLKRST_CLK_EN Configures whether to force enable the clock gate for header registers.
- O: Invalid
- 1: Force enable (R/W)
```