

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.56. GPIO_EXT_ETM_TASK_P7_CFG_REG (0x00BC)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO31_SEL | GPIO_EXT_ETM_TASK_GPIO31_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO30_SEL | GPIO_EXT_ETM_TASK_GPIO30_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO29_SEL | GPIO_EXT_ETM_TASK_GPIO29_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO28_SEL | GPIO_EXT_ETM_TASK_GPIO28_EN | Reset |
| Value | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 |

GPIO_EXT_ETM_TASK_GPIOn_EN (n: 28 - 31) Configures whether or not to enable GPIOn to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIOn_SEL (n: 28 - 31) Configures to select an ETM task channel for GPIOn.
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```