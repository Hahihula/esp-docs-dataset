

```markdown
Register 19.86. PMS_HP_COREn_MM_PMS_REGO_REG (n: 0-1) (0x0008+0x8*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | Reset |

PMS_HP_COREn_MM_LP_SYSREG_ALLOW Configures whether HP CPU in machine mode has permission to access LP System Registers.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_MM_LP_AONCLKRST_ALLOW Configures whether HP CPU in machine mode has permission to access LP_AONCLKRST.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_MM_LP_TIMER_ALLOW Configures whether HP CPU in machine mode has permission to access LP timer.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_MM_LP_ANAPERI_ALLOW Configures whether HP CPU in machine mode has permission to access LP ANAPERI.
O: Not allowed
1: Allowed
(R/W)

PMS_HP_COREn_MM_LP_PMU_ALLOW Configures whether HP CPU in machine mode has permission to access LP PMU.
O: Not allowed
1: Allowed
(R/W)
```
Continued on the next page...
```