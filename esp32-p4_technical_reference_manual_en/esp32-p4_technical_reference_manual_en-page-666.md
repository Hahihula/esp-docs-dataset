

```markdown
Register 10.8. HP_SYS_CLKRST_SOC_CLK_CTRL2_REG (0x001C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 0 |
|     |    |   |    |    |    |    |    |    |    |    |    |    | Reset |

HP_SYS_CLKRST_RMT_SYS_CLK_EN Configures whether to enable the bus clock of RMT (SYS_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_HP_CLKRST_APB_CLK_EN Configures whether to enable the bus clock of the Reset and Clock module (APB_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_SYSREG_APB_CLK_EN Configures whether to enable the bus clock of the HP System Registers (APB_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_ICM_APB_CLK_EN Configures the bus clock of the bus module (APB_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_INTRMTX_APB_CLK_EN Configures whether to enable the bus clock of the Interrupt Matrix (APB_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_ADC_APB_CLK_EN Configures whether to enable the bus clock of the ADC (APB_CLK clock domain).
O: Disable
1: Enable
(R/W)
```
Continued on the next page...
```