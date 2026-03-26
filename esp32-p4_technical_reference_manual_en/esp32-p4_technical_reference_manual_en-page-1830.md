

```markdown
Register 38.14. LCD_CAM_CAM_RGB_YUV_REG (0x000C)

Continued from the previous page...

LCD_CAM_CAM_CONV_DATA_IN_MODE Configures the color range for the YUV-RGB converter's input data.
O: Limited color range.
1: Full color range.
(R/W)

LCD_CAM_CAM_CONV_MODE_8BITS_ON Configures the bit width of the YUV-RGB converter's input data.
O: 16-bit mode.
1: 8-bit mode.
(R/W)

LCD_CAM_CAM_CONV_TRANS_MODE Configures the data conversion format.
O: Data is converted to RGB format.
1: Data is converted to YUV format.
(R/W)

LCD_CAM_CAM_CONV_ENABLE Configures whether to enable the YUV-RGB converter.
O: Bypass.
1: Enable.
(R/W)

Register 38.15. LCD_CAM_LC_DMA_INT_ENA_REG (0x0064)
```
```markdown
| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 31-4|             |
| 4   | LCD_CAM_LCD_VSYNC_INT_ENA Write 1 to enable LCD_CAM_LCD_VSYNC_INT. (R/W) |
| 3   | LCD_CAM_LCD_TRANS_DONE_INT_ENA Write 1 to enable LCD_CAM_LCD_TRANS_DONE_INT. (R/W) |
| 2   | LCD_CAM_CAM_VSYNC_INT_ENA Write 1 to enable LCD_CAM_CAM_VSYNC_INT. (R/W) |
| 1   | LCD_CAM_CAM_HS_INT_ENA Write 1 to enable LCD_CAM_CAM_HS_INT. (R/W) |
| 0   | Reset |
```