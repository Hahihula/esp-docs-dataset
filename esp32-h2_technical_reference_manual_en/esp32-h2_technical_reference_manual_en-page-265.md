

```markdown
Register 6.32. GPIO_EXT_ETM_TASK_P4_CFG_REG (0x00B0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO19_SEL | GPIO_EXT_ETM_TASK_GPIO19_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO18_SEL | GPIO_EXT_ETM_TASK_GPIO18_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO17_SEL | GPIO_EXT_ETM_TASK_GPIO17_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO16_SEL | GPIO_EXT_ETM_TASK_GPIO16_EN | Reset |
| Value | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 |

GPIO_EXT_ETM_TASK_GPIO_EN (n = 16 ~ 19) Configures whether or not to enable GPIO[n] to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO_SEL (n = 16 ~ 19) Configures to select an ETM task channel for GPIO[n].
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```