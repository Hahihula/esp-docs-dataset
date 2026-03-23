

```markdown
Register 7.31. GPIO_EXT_ETM_TASK_P5_CFG_REG (0x00B4)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | GPIO_EXT_ETM_TASK_GPIO23_SEL<br>(reserved)<br>GPIO_EXT_ETM_TASK_GPIO23_EN<br>(reserved)<br>GPIO_EXT_ETM_TASK_GPIO21_SEL<br>(reserved)<br>GPIO_EXT_ETM_TASK_GPIO21_EN<br>(reserved)<br>GPIO_EXT_ETM_TASK_GPIO20_SEL<br>(reserved)<br>GPIO_EXT_ETM_TASK_GPIO20_EN |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

GPIO_EXT_ETM_TASK_GPIOn_EN (n: 20 - 23) Configures whether or not to enable GPIOn to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIOn_SEL (n: 20 - 23) Configures to select an ETM task channel for GPIOn.
O: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```