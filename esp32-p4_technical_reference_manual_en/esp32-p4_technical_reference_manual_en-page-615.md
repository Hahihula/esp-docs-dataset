

```markdown
Register 9.57. GPIO_EXT_ETM_TASK_P8_CFG_REG (0x00C0)

31       28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
[reserved] GPIO_EXT_ETM_TASK_GPIO35_SEL
GPIO_EXT_ETM_TASK_GPIO35_EN [reserved]
GPIO_EXT_ETM_TASK_GPIO34_SEL
GPIO_EXT_ETM_TASK_GPIO34_EN [reserved]
GPIO_EXT_ETM_TASK_GPIO33_SEL
GPIO_EXT_ETM_TASK_GPIO33_EN [reserved]
GPIO_EXT_ETM_TASK_GPIO32_SEL
GPIO_EXT_ETM_TASK_GPIO32_EN

0 0 0 0x0 0 0 0 0 0x0 0 0 0 0 0x0 0 0 0x0 0 0 Reset

GPIO_EXT_ETM_TASK_GPIOn_EN (n: 32 - 35) Configures whether or not to enable GPIOn to re-
sponse ETM task.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_ETM_TASK_GPIOn_SEL (n: 32 - 35) Configures to select an ETM task channel for
GPIOn.
O: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)
```