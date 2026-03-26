

```markdown
Register 9.59. GPIO_EXT_ETM_TASK_P10_CFG_REG (0x00C8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | Reset|

GPIO_EXT_ETM_TASK_GPIO_EN (n: 40 - 43) Configures whether or not to enable GPIO[n] to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO_SEL (n: 40 - 43) Configures to select an ETM task channel for GPIO[n].
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```