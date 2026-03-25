

```markdown
Register 8.33. GPIO_EXT_ETM_TASK_PO_CFG_REG (0x0158)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | (reserved) | GPIO_EXT_ETM_TASK_GPIO1_SEL | GPIO_EXT_ETM_TASK_GPIO2_SEL | GPIO_EXT_ETM_TASK_GPIO3_SEL | GPIO_EXT_ETM_TASK_GPIO4_SEL | GPIO_EXT_ETM_TASK_GPIO5_EN | GPIO_EXT_ETM_TASK_GPIO6_EN | GPIO_EXT_ETM_TASK_GPIO7_EN | Reset |

GPIO_EXT_ETM_TASK_GPIO0_SEL Configures to select an ETM task channel for GPIO0.
O: Select channel 0
1: Select channel 1

......

7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO0_EN Configures whether or not to enable GPIO0 to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO1_SEL Configures to select an ETM task channel for GPIO1.
O: Select channel 0
1: Select channel 1

......

7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO1_EN Configures whether or not to enable GPIO1 to response ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIO2_SEL Configures to select an ETM task channel for GPIO2.
O: Select channel 0
1: Select channel 1

......

7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO2_EN Configures whether or not to enable GPIO2 to response ETM task.
O: Not enable
1: Enable
(R/W)
```
Continued on the next page...
```