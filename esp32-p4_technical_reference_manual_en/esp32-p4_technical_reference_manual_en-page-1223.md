

```markdown
Register 19.77: PMS_LP_MM_LP_PERI_PMS_REGO_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | Reset |

PMS_LP_MM_LP_SYSREG_ALLOW Configures whether LP CPU in machine mode has permission to access LP system registers.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_AONCLKRST_ALLOW Configures whether LP CPU in machine mode has permission to access LP_AONCLKRST (LP always-on clock and reset).
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_TIMER_ALLOW Configures whether LP CPU in machine mode has permission to access LP timer.
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_ANAPERI_ALLOW Configures whether LP CPU in machine mode has permission to access LP ANAPERI (analog peripherals).
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_PMU_ALLOW Configures whether LP CPU in machine mode has permission to access LP PMU (Power Management Unit).
O: Not allowed
1: Allowed
(R/W)

PMS_LP_MM_LP_WDT_ALLOW Configures whether LP CPU in machine mode has permission to access LP WDT (watchdog timer).
O: Not allowed
1: Allowed
(R/W)

Continued on the next page...
```