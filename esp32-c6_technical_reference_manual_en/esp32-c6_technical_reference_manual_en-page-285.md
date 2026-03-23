

```markdown
Register 7.24. GPIO_EXT_GLITCH_FILTER_CHn_REG (n: 0-7) (0x0030+0x4*n)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                |                                                                             |
| 19..18    | GPIO_EXT_FILTER_CHn_WINDOW_WIDTH          | Configures the window threshold for Glitch Filter. The window threshold should be less than or equal to GPIO_EXT_FILTER_CHn_WINDOW_WIDTH. Measurement unit: IO MUX operating clock cycle (R/W) |
| 13..7     | GPIO_EXT_FILTER_CHn_WINDOW_THRES          | Configures the window width for Glitch Filter. The effective value of window width is 0 ~ 62. 63 is a reserved value and cannot be used. Measurement unit: IO MUX operating clock cycle (R/W) |
| 1..0      | GPIO_EXT_FILTER_CHn_INPUT_IO_NUM          | Configures to select the input GPIO for Glitch Filter.<br>0: Select GPIO0<br>1: Select GPIO1<br>......<br>29: Select GPIO29<br>30: Select GPIO30 (R/W) |
| 0         | GPIO_EXT_FILTER_CHn_EN                    | Configures whether or not to enable channel n of Glitch Filter.<br>0: Not enable<br>1: Enable (R/W) |

GPIO_EXT_FILTER_CHn_INPUT_IO_NUM Configures to select the input GPIO for Glitch Filter.
0: Select GPIO0
1: Select GPIO1
......
29: Select GPIO29
30: Select GPIO30
(R/W)

GPIO_EXT_FILTER_CHn_WINDOW_THRES Configures the window threshold for Glitch Filter. The window threshold should be less than or equal to GPIO_EXT_FILTER_CHn_WINDOW_WIDTH.
Measurement unit: IO MUX operating clock cycle
(R/W)

GPIO_EXT_FILTER_CHn_WINDOW_WIDTH Configures the window width for Glitch Filter. The effective value of window width is 0 ~ 62. 63 is a reserved value and cannot be used.
Measurement unit: IO MUX operating clock cycle
(R/W)
```