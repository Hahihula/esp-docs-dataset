

```markdown
Register 9.47. GPIO_EXT_GLITCH_FILTER_CHn_REG (n: 0 - 7) (0x0030+0x4*n)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-6      | (reserved)                                |                                                                             |
| 5         | GPIO_EXT_FILTER_CHn_INPUT_IO_NUM          | Configures to select the input GPIO for Glitch Filter.                      |
|           |                                            | 0: Select GPIO0                                                               |
|           |                                            | 1: Select GPIO1                                                               |
|           |                                            | ......                                                                       |
|           |                                            | 53: Select GPIO53                                                             |
|           |                                            | 54: Select GPIO54                                                             |
|           | (R/W)                                     |                                                                             |
| 4         | GPIO_EXT_FILTER_CHn_WINDOW_THRES          | Configures the window threshold for Glitch Filter. The                    |
|           |                                            | window threshold should be less than or equal to GPIO_EXT_FILTER_CHn_WINDOW_WIDTH. |
|           | Measurement unit: HP IO MUX operating clock cycle | (R/W)                                                                         |
| 3         | GPIO_EXT_FILTER_CHn_WINDOW_WIDTH          | Configures the window width for Glitch Filter. The effective value of window width is 0 ~ 62. 63 is a reserved value and cannot be used. |
|           | Measurement unit: HP IO MUX operating clock cycle | (R/W)                                                                         |

GPIO_EXT_FILTER_CHn_EN   Configures whether or not to enable channel n of Glitch Filter.
O: Not enable
1: Enable
(R/W)

GPIO_EXT_FILTER_CHn_INPUT_IO_NUM  Configures to select the input GPIO for Glitch Filter.

GPIO_EXT_FILTER_CHn_WINDOW_THRES  Configures the window threshold for Glitch Filter. The window threshold should be less than or equal to GPIO_EXT_FILTER_CHn_WINDOW_WIDTH.
Measurement unit: HP IO MUX operating clock cycle
(R/W)

GPIO_EXT_FILTER_CHn_WINDOW_WIDTH   Configures the window width for Glitch Filter. The effective value of window width is 0 ~ 62. 63 is a reserved value and cannot be used.
Measurement unit: HP IO MUX operating clock cycle
(R/W)
```