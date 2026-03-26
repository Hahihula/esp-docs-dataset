

```markdown
Register 10.6. HP_SYS_CLKRST_SOC_CLK_CTRL0_REG (0x0014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 1 | 1 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0 | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 | Reset |

HP_SYS_CLKRST_CORE0_CLIC_CLK_EN Configures whether to enable the bus clock of HP CPU0 CLIC.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CORE1_CLIC_CLK_EN Configures whether to enable the bus clock of HP CPU1 CLIC.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_MISC_CPU_CLK_EN Configures whether to enable the bus clock of miscellaneous modules (CPU_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CORE0_CPU_CLK_EN Configures whether to enable the bus clock of HP CPU0 (CPU_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CORE1_CPU_CLK_EN Configures whether to enable the bus clock of HP CPU1 (CPU_CLK clock domain).
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_SPM_CPU_CLK_EN Configures whether to enable the bus clock of SPM monitor (CPU_CLK clock domain).
O: Disable
1: Enable
(R/W)
```
Continued on the next page...
```