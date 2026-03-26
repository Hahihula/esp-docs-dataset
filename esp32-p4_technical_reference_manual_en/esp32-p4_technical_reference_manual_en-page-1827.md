

```markdown
Register 38.13. LCD_CAM_CAM_CTRL1_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | LCD_CAM_CAM_AFIFO_RESET | LCD_CAM_CAM_RESET | LCD_CAM_CAM_START | LCD_CAM_CAM_VH_DE_MODE_EN | LCD_CAM_CAM_VSYNC_INV | LCD_CAM_CAM_HSYNC_2BYTE_EN | LCD_CAM_CAM_LINE_INT_NUM | LCD_CAM_CAM_CLK_INV | LCD_CAM_CAM_VSYNC_FILTER_EN | LCD_CAM_CAM_DATA_BYTELEN |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0x00 |

LCD_CAM_CAM_REC_DATA_BYTELEN Configures the data byte length received by the Camera module. When the length of received data reaches this value + 1, GDMA in_suc_eof_int is triggered. (R/W)

LCD_CAM_CAM_LINE_INT_NUM Configures the number of video lines. When the number of video lines reaches this value + 1, LCD_CAM_CAM_HS_INT is triggered. (R/W)

LCD_CAM_CAM_CLK_INV Configures whether to invert the input signal CAM_PCLK.
0: Do not invert.
1: Invert.
(R/W)

LCD_CAM_CAM_VSYNC_FILTER_EN Configures whether to enable CAM_VSYNC filter function.
0: Bypass.
1: Enable.
(R/W)

LCD_CAM_CAM_2BYTE_EN Configures the width of input data.
0: 8 bits.
1: 16 bits.
(R/W)

LCD_CAM_CAM_DE_INV Configures whether to invert the input signal CAM_DE.
0: Do not invert.
1: Invert.
(R/W)

LCD_CAM_CAM_HSYNC_INV Configures whether to invert the input signal CAM_HSYNC.
0: Do not invert.
1: Invert.
(R/W)

LCD_CAM_CAM_VSYNC_INV Configures whether to invert the input signal CAM_VSYNC.
0: Do not invert.
1: Invert.
(R/W)
```