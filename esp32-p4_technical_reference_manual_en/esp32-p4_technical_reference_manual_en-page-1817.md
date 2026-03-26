

```markdown
Chapter 38 LCD and Camera Controller (LCD_CAM)                                     GoBack

Register 38.2. LCD_CAM_LCD_RGB_YUV_REG (0x0010)

Continued from the previous page...

LCD_CAM_LCD_CONV_DATA_IN_MODE   Configures the color range for input data.
    0: Limited color range.
    1: Full color range.
    (R/W)

LCD_CAM_LCD_CONV_MODE_8BITS_ON   Configures the valid bit width of the YUV-RGB converter’s
    input data.
    0: 16 bits.
    1: 8 bits.
    (R/W)

LCD_CAM_LCD_CONV_TRANS_MODE   Configures the RGB or YUV format for data conversion.
    0: Converted to RGB format.
    1: Converted to YUV format.
    (R/W)

LCD_CAM_LCD_CONV_ENABLE   Configures whether to enable YUV-RGB converter.
    0: Bypass the converter.
    1: Enable the converter.
    (R/W)
```