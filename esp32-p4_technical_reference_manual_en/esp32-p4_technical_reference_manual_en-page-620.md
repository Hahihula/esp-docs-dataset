

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.62. GPIO_EXT_ETM_TASK_P13_CFG_REG (0x00D4)

| Bit | Field Name                     |
|-----|--------------------------------|
| 31  | (reserved)                    |
| 30-28| GPIO_EXT_ETM_TASK_GPIO64_SEL   |
| 27-25| GPIO_EXT_ETM_TASK_GPIO64_EN    |
| 24-22| (reserved)                   |
| 21-19| GPIO_EXT_ETM_TASK_GPIO63_SEL   |
| 18-16| GPIO_EXT_ETM_TASK_GPIO63_EN    |
| 15-13| (reserved)                  |
| 12-10| GPIO_EXT_ETM_TASK_GPIO62_SEL   |
| 9-7  | GPIO_EXT_ETM_TASK_GPIO62_EN    |
| 6-4  | (reserved)                   |
| 3-1  | GPIO_EXT_ETM_TASK_GPIO61_SEL   |
| 0    | Reset                        |

GPIO_EXT_ETM_TASK_GPIOn_EN (n: 52 - 54) Configures whether or not to enable GPIOn to re-
sponse ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIOn_SEL (n: 52 - 54) Configures to select an ETM task channel for
GPIOn.
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)

Register 9.63. GPIO_EXT_VERSION_REG (0xO0FC)

| Bit | Field Name         |
|-----|--------------------|
| 31  | (reserved)        |
| 30-28|                    |
| 27  | GPIO_EXT_DATE     |
| 26-0 | 0x2203050 Reset   |

GPIO_EXT_DATE Version control register.
(R/W)

9.20.4 LP GPIO Matrix Registers

The addresses in this section are relative to LP GPIO matrix base address provided in Table 7.3-2 in Chapter 7
System and Memory.

For how to program reserved fields, please refer to Section IX .
```