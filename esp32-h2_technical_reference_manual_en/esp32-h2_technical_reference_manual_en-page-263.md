

```markdown
Register 6.30. GPIO_EXT_ETM_TASK_P2_CFG_REG (0x00A8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO1_SEL | GPIO_EXT_ETM_TASK_GPIO1_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO0_SEL | GPIO_EXT_ETM_TASK_GPIO0_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO9_SEL | GPIO_EXT_ETM_TASK_GPIO9_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO8_SEL | GPIO_EXT_ETM_TASK_GPIO8_EN | Reset |
| Value | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 |

GPIO_EXT_ETM_TASK_GPIOn_EN (n = 8 ~ 11) Configures whether or not to enable GPIOn to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIOn_SEL (n = 8 ~ 11) Configures to select an ETM task channel for GPIOn.
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```