

```markdown
Register 10.2. HP_SYS_CLKRST_ROOT_CLK_CTRL0_REG (0x0004)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | O                                          |                                                                             |
| 29  | O                                          |                                                                             |
| 28  | HP_SYS_CLKRST_CPU_CLK_DIV_DENOMINATOR      | Configures the denominator of the divisor's fractional part for CPU_CLK. (R/W)|
| 27  | HP_SYS_CLKRST_CPU_CLK_DIV_NUMERATOR        | Configures the numerator of the divisor's fractional part for CPU_CLK. (R/W) |
| 26  | O                                          |                                                                             |
| 25  | O                                          |                                                                             |
| 24  | HP_SYS_CLKRST_CPU_CLK_DIV_NUM              | Configures the integer part of the CPU_CLK clock divisor. (R/W)               |
| 23  | O                                          |                                                                             |
| 22  | O                                          |                                                                             |
| 21  | HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE           | Configures whether to update the divisors for CPU_CLK, MEM_CLK, SYS_CLK, APB_CLK. (R/W)|
|     |                                             | 0: Not update<br>1: Update (WT)                                            |
| 20  | O                                          |                                                                             |
| 19  | O                                          |                                                                             |
| 18  | HP_SYS_CLKRST_CPU_CLK_DELAY_NUM            | Configures the time required from entering WFI mode to the actual shutdown of the CPU clock. Measurement unit: clock cycles. (R/W)|
|     |                                             |                                                                             |
```

HP_SYS_CLKRST_CPU_CLK_DELAY_NUM Configures the time required from entering WFI mode to the actual shutdown of the CPU clock.
Measurement unit: clock cycles. (R/W)

HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE Configures whether to update the divisors for CPU_CLK, MEM_CLK, SYS_CLK, APB_CLK.
0: Not update
1: Update (WT)

HP_SYS_CLKRST_CPU_CLK_DIV_NUM Configures the integer part of the CPU_CLK clock divisor. (R/W)

HP_SYS_CLKRST_CPU_CLK_DIV_NUMERATOR Configures the numerator of the divisor's fractional part for CPU_CLK. (R/W)

HP_SYS_CLKRST_CPU_CLK_DIV_DENOMINATOR Configures the denominator of the divisor's fractional part for CPU_CLK. (R/W)
```