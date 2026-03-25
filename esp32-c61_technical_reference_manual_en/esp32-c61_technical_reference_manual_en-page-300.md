

```markdown
| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30  | GPIO_EXT_ETM_TASK_GPIO4_EN          |                                                                             |
| 29  | (reserved)                          |                                                                             |
| 28  | GPIO_EXT_ETM_TASK_GPIO3_EN          |                                                                             |
| 27  | (reserved)                          |                                                                             |
| 26  | GPIO_EXT_ETM_TASK_GPIO2_EN          |                                                                             |
| 25  | (reserved)                          |                                                                             |
| 24  | GPIO_EXT_ETM_TASK_GPIO1_EN          |                                                                             |
| 23  | (reserved)                          |                                                                             |
| 22  | GPIO_EXT_ETM_TASK_GPIO0_EN          |                                                                             |
| 21  | (reserved)                          |                                                                             |
| 20  | O                                   | 0x0                                                                          |
| 19  | O                                   | 0x0                                                                          |
| 18  | O                                   | 0x0                                                                          |
| 17  | O                                   | 0x0                                                                          |
| 16  | O                                   | 0x0                                                                          |
| 15  | O                                   | 0x0                                                                          |
| 14  | O                                   | 0x0                                                                          |
| 13  | O                                   | 0x0                                                                          |
| 12  | O                                   | 0x0                                                                          |
| 11  | O                                   | 0x0                                                                          |
| 10  | O                                   | 0x0                                                                          |
| 9   | O                                   | 0x0                                                                          |
| 8   | (reserved)                          |                                                                             |
| 7   | GPIO_EXT_ETM_TASK_GPIO0_SEL         | Select channel 0                                                             |
| 6   | GPIO_EXT_ETM_TASK_GPIO1_SEL         | Select channel 0                                                             |
| 5   | GPIO_EXT_ETM_TASK_GPIO2_SEL         | Select channel 0                                                             |
| 4   | GPIO_EXT_ETM_TASK_GPIO3_SEL         | Select channel 0                                                             |
| 3   | GPIO_EXT_ETM_TASK_GPIO4_SEL         | Select channel 0                                                             |
| 2   | (reserved)                          |                                                                             |
| 1   | O                                   | 0x0                                                                          |
| 0   | Reset                               |                                                                                 |

---

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