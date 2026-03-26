

```markdown
Register 9.52. GPIO_EXT_ETM_TASK_P3_CFG_REG (0x00AC)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     |    |    |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO15_SEL | GPIO_EXT_ETM_TASK_GPIO15_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO14_SEL | GPIO_EXT_ETM_TASK_GPIO14_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO13_SEL | GPIO_EXT_ETM_TASK_GPIO13_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO12_SEL | GPIO_EXT_ETM_TASK_GPIO12_EN |
|     | 0  | 0  | 0  | 0x0 | 0   | 0   | 0   | 0x0 | 0   | 0   | 0   | 0x0 | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | Reset |

GPIO_EXT_ETM_TASK_GPIO_EN (n: 12 - 15) Configures whether or not to enable GPIO_n to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO_SEL (n: 12 - 15) Configures to select an ETM task channel for GPIO_n.
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```