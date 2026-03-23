

```markdown
Register 7.33. GPIO_EXT_ETM_TASK_P7_CFG_REG (0x00BC)

| Bit | Field Description                                                                 |
|-----|------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                        |
| 30  | GPIO_EXT_ETM_TASK_GPIO30_SEL                                                       |
| 29  | GPIO_EXT_ETM_TASK_GPIO30_EN                                                        |
| 28  | GPIO_EXT_ETM_TASK_GPIO29_SEL                                                       |
| 27  | GPIO_EXT_ETM_TASK_GPIO29_EN                                                        |
| 26  | (reserved)                                                                        |
| 25  | GPIO_EXT_ETM_TASK_GPIO28_SEL                                                       |
| 24  | GPIO_EXT_ETM_TASK_GPIO28_EN                                                        |
| 23  | (reserved)                                                                        |
| 22  | GPIO_EXT_ETM_TASK_GPIO07_SEL                                                       |
| 21  | GPIO_EXT_ETM_TASK_GPIO07_EN                                                        |
| 20  | (reserved)                                                                        |
| 19  | GPIO_EXT_ETM_TASK_GPIO06_SEL                                                       |
| 18  | GPIO_EXT_ETM_TASK_GPIO06_EN                                                        |
| 17  | (reserved)                                                                        |
| 16  | GPIO_EXT_ETM_TASK_GPIO05_SEL                                                       |
| 15  | GPIO_EXT_ETM_TASK_GPIO05_EN                                                        |
| 14  | (reserved)                                                                        |
| 13  | GPIO_EXT_ETM_TASK_GPIO04_SEL                                                       |
| 12  | GPIO_EXT_ETM_TASK_GPIO04_EN                                                        |
| 11  | (reserved)                                                                        |
| 10  | GPIO_EXT_ETM_TASK_GPIO03_SEL                                                       |
| 9   | GPIO_EXT_ETM_TASK_GPIO03_EN                                                        |
| 8   | (reserved)                                                                        |
| 7   | GPIO_EXT_ETM_TASK_GPIO02_SEL                                                       |
| 6   | GPIO_EXT_ETM_TASK_GPIO02_EN                                                        |
| 5   | (reserved)                                                                        |
| 4   | GPIO_EXT_ETM_TASK_GPIO01_SEL                                                       |
| 3   | GPIO_EXT_ETM_TASK_GPIO01_EN                                                        |
| 2   | (reserved)                                                                        |
| 1   | GPIO_EXT_ETM_TASK_GPIO00_SEL                                                       |
| 0   | GPIO_EXT_ETM_TASK_GPIO00_EN                                                        |

GPIO_EXT_ETM_TASK_GPIOn_EN (n: 28 - 30) Configures whether or not to enable GPIOn to re-
sponse ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIOn_SEL (n: 28 - 30) Configures to select an ETM task channel for
GPIOn.
O: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)


Register 7.34. GPIO_EXT_VERSION_REG (0x00FC)

| Bit | Field Description |
|-----|-------------------|
| 31  | (reserved)        |
| 30  |                   |
| 29  |                   |
| 28  |                   |
| 27  |                   |
| 26  |                   |
| 25  |                   |
| 24  |                   |
| 23  |                   |
| 22  |                   |
| 21  |                   |
| 20  |                   |
| 19  |                   |
| 18  |                   |
| 17  |                   |
| 16  |                   |
| 15  |                   |
| 14  |                   |
| 13  |                   |
| 12  |                   |
| 11  |                   |
| 10  |                   |
| 9   |                   |
| 8   |                   |
| 7   |                   |
| 6   |                   |
| 5   |                   |
| 4   |                   |
| 3   |                   |
| 2   |                   |
| 1   |                   |
| 0   | GPIO_EXT_DATE     |

GPIO_EXT_DATE Version control register.
(R/W)


7.16.4 LP IO MUX Registers

The addresses in this section are relative to LP_IO base address provided in Table 5.3-2 in Chapter 5 System
and Memory.
```