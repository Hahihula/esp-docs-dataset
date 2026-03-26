

```markdown
Register 38.11. LCD_CAM_LCD_DLY_MODE_CFG2_REG (0x0038)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | 0xO | Reset |

LCD_CAM_DOUTn_MODE (n: 0 - 15) Configures the delay of the output data bit n.

0: No delay.
1: Delayed at the rising edge of LCD_CLK.
2: Delayed at the falling edge of LCD_CLK.
(R/W)
```