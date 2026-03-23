

```markdown
Register 7.37. LP_IO_OUT_W1TC_REG (0x0008)
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
|     | [reserved] | 0 | Reset |
LP_GPIO_OUT_DATA_W1TC Configures whether or not to clear the output register LP_IO_OUT_REG of GPIO0 ~ GPIO7.
* bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
* If the value 1 is written to a bit here, the corresponding bit in LP_IO_OUT_REG will be cleared.
* Recommended operation: use this register to clear LP_IO_OUT_REG.

Register 7.38. LP_IO_ENABLE_REG (0x000C)
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
|     | [reserved] | 0 | Reset |
LP_GPIO_ENABLE Configures whether or not to enable the output of GPIO0 ~ GPIO7.
0: Not enable
1: Enable
bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
(R/W)
```