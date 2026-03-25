

```markdown
Register 6.26. GPIO_EXT_GLITCH_FILTER_CHn_REG (n: 0-7) (0x0030+0x4*n)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                 |                                                                             |
| 19..18    | GPIO_EXT_FILTER_CHn_WINDOW_WIDTH           | Configures the window threshold for Glitch Filter. The window threshold should be less than or equal to GPIO_EXT_FILTER_CHn_WINDOW_WIDTH. Measurement unit: IO MUX operating clock cycle (R/W) |
| 13..12    | GPIO_EXT_FILTER_CHn_WINDOW_THRES           | Configures the window width for Glitch Filter. The valid range for the window width is 0 ~ 62, and 63 is a reserved value that cannot be used. Measurement unit: IO MUX operating clock cycle (R/W) |
| 7..6      | GPIO_EXT_FILTER_CHn_INPUT_IO_NUM           | Configures to select the input GPIO for Glitch Filter.<br>0: Select GPIO0<br>1: Select GPIO1<br>......<br>26: Select GPIO26<br>27: Select GPIO27 (R/W) |
| 1..0      | GPIO_EXT_FILTER_CHn_EN                     | Configures whether or not to enable channel n of Glitch Filter.<br>0: Not enable<br>1: Enable (R/W) |

```
```plaintext
+-------+--------+--------+--------+
|31     |19 18   |13 12   |7 6     |
+-------+--------+--------+--------+
|reserved|GPIO_EXT_FILTER_CHn_WINDOW_WIDTH|GPIO_EXT_FILTER_CHn_WINDOW_THRES|GPIO_EXT_FILTER_CHn_INPUT_IO_NUM|
+-------+--------+--------+--------+
|0x0   |0x0    |0x0    |0      |
+-------+--------+--------+--------+
Reset
```