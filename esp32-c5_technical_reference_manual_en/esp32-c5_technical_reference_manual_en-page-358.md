

```markdown
Register 8.31. GPIO_EXT_GLITCH_FILTER_CHn_REG (n: 0-7) (0x00D8+0x4*n)

| 31 | 20 | 19 | 14 | 13 | 8 | 7 | 6 | 1 | 0 |
|-----|----:|----:|----:|----:|---:|---:|---:|---:|---:|
| 0   |  0  |  0  |  0  | 0x0 | 0x0 |  0 | 0x0 |  0 | Reset |

GPIO_EXT_FILTER_CHn_EN Configures whether or not to enable channel n of Glitch Filter.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_FILTER_CHn_INPUT_IO_NUM Configures to select the input GPIO for Glitch Filter.
0: Select GPIO0
1: Select GPIO1
......
27: Select GPIO27
28: Select GPIO28
29~63: Reserved
(R/W)

GPIO_EXT_FILTER_CHn_WINDOW_THRES Configures the window threshold for Glitch Filter. The window threshold should be less than or equal to GPIO_EXT_FILTER_CHn_WINDOW_WIDTH.
Measurement unit: IO MUX operating clock cycle
(R/W)

GPIO_EXT_FILTER_CHn_WINDOW_WIDTH Configures the window width for Glitch Filter.
The effective value of window width is 0~63.
Measurement unit: IO MUX operating clock cycle
(R/W)
```