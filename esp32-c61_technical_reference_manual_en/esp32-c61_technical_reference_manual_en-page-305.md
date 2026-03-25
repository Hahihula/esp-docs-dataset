
```markdown
Chapter 6 GPIO Matrix and IO MUX

Register 6.32. GPIO_EXT_ETM_TASK_P2_CFG_REG (0x0160)

Continued from the previous page...

GPIO_EXT_ETM_TASK_GPIO13_SEL Configures to select an ETM task channel for GPIO13.
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO13_EN Configures whether or not to enable GPIO13 to response ETM task.
O: Not enable
1: Enable
(R/W)


Register 6.33. GPIO_EXT_ETM_TASK_P4_CFG_REG (0x0168)
```

```plaintext
(reserved)       GPIO_EXT_ETM_TASK_GPIO24_EN      (reserved)   GPIO_EXT_ETM_TASK_GPIO24_SEL
                 GPIO_EXT_ETM_TASK_GPIO23_EN      (reserved)   GPIO_EXT_ETM_TASK_GPIO23_SEL
                 GPIO_EXT_ETM_TASK_GPIO22_EN      (reserved)   GPIO_EXT_ETM_TASK_GPIO22_SEL

Bit:  31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10  9  8  7  6  5  4  3  2  1  0
Value: 0   0  0  0  0  0x0 0  0  0  0  0x0 0  0  0  0  0  0x0 0  0  0  0x0 (reserved) (reserved) (reserved) (reserved) (reserved)
Reset:   O  O  O  O
```

```markdown
GPIO_EXT_ETM_TASK_GPIO22_SEL Configures to select an ETM task channel for GPIO22.
0: Select channel 0
1: Select channel 1
......
7: Select channel 7
(R/W)

GPIO_EXT_ETM_TASK_GPIO22_EN Configures whether or not to enable GPIO22 to response ETM task.
O: Not enable
1: Enable
(R/W)

Continued on the next page...
```