

```markdown
Register 8.36. GPIO_EXT_ETM_TASK_P4_CFG_REG (0x0168)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 16 | 15 | 14 | 12 | 11 | 10 | 9 | 8 | 6 | 5 | 4 | 3 | 2 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | GPIO_EXT_ETM_TASK_GPIO24_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO23_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO24_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO23_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO23_EN | (reserved) | GPIO_EXT_ETM_TASK_GPIO24_SEL | (reserved) | GPIO_EXT_ETM_TASK_GPIO24_EN | (reserved) | Reset |
| Value | 0 | 0 | 0 | 0 | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO |

GPIO_EXT_ETM_TASK_GPIO23_SEL Configures to select an ETM task channel for GPIO23.
- O: Select channel 0
- 1: Select channel 1
```
```markdown
......
- 7: Select channel 7

(R/W)

GPIO_EXT_ETM_TASK_GPIO23_EN Configures whether or not to enable GPIO23 to response ETM task.
- O: Not enable
- 1: Enable

(R/W)
```
```markdown
GPIO_EXT_ETM_TASK_GPIO24_SEL Configures to select an ETM task channel for GPIO24.
- O: Select channel 0
- 1: Select channel 1
```
```markdown
......
- 7: Select channel 7

(R/W)

GPIO_EXT_ETM_TASK_GPIO24_EN Configures whether or not to enable GPIO24 to response ETM task.
- O: Not enable
- 1: Enable

(R/W)
```

Espressif Systems
366
ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```