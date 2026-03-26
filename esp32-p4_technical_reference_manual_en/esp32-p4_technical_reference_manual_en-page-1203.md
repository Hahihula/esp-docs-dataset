

```markdown
Register 19.67. PMS_COREn_UM_HP_PERI_PMS_REG2_REG (n: 0–1) (0x0020+0x20*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 1   | 0  | 1  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | Reset |

PMS_COREn_UM_HP_MCPWM0_ALLOW Configures whether HP CPU in user mode has permission to access HP MCPWM0.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_MCPWM1_ALLOW Configures whether HP CPU in user mode has permission to access HP MCPWM1.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_TIMER_GROUPO_ALLOW Configures whether HP CPU in user mode has permission to access HP timer group0.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_TIMER_GROUP1_ALLOW Configures whether HP CPU in user mode has permission to access HP timer group1.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_I2C0_ALLOW Configures whether HP CPU in user mode has permission to access HP I2C0.
O: Not allowed
1: Allowed
(R/W)

PMS_COREn_UM_HP_I2C1_ALLOW Configures whether HP CPU in user mode has permission to access HP I2C1.
O: Not allowed
1: Allowed
(R/W)
```