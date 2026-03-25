

```markdown
Register 6.31. GPIO_EXT_ETM_TASK_P1_CFG_REG (0x015C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | GPIO_EXT_ETM_TASK_GPIO9_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO8_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO7_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO6_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO5_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO4_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO3_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO2_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO1_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO0_SEL | Reset |
| Value | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

GPIO_EXT_ETM_TASK_GPIO5_SEL Configures to select an ETM task channel for GPIO5.
O: Select channel 0
1: Select channel 1

......

7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO5_EN Configures whether or not to enable GPIO5 to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO6_SEL Configures to select an ETM task channel for GPIO6.
O: Select channel 0
1: Select channel 1

......

7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO6_EN Configures whether or not to enable GPIO6 to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO7_SEL Configures to select an ETM task channel for GPIO7.
O: Select channel 0
1: Select channel 1

......

7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO7_EN Configures whether or not to enable GPIO7 to response ETM task.
O: Not enable
1: Enable
(R/W)
```