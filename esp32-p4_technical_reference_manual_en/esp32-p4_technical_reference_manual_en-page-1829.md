

```markdown
Register 38.14. LCD_CAM_CAM_RGB_YUV_REG (0x000C)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | LCD_CAM_CAM_CONV_ENABLE                   |
| 30  | LCD_CAM_CAM_CONV_TRAN_MODE                |
| 29  | LCD_CAM_CAM_CONV_8BITS_INV                |
| 28  | LCD_CAM_CAM_CONV_DATA_IN                  |
| 27  | LCD_CAM_CAM_CONV_OUT_MODE                 |
| 26  | LCD_CAM_CAM_CONV_PROTOCOL_MODE            |
| 25  | LCD_CAM_CAM_CONV_YUV2YUV_MODE             |
| 24  | LCD_CAM_CAM_CONV_YUV_MODE                 |
| 23  | (reserved)                                |
| 22  |                                            |
| 21  |                                            |
| ... | ...                                        |

0   0   0   0   0   0   0   3   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   Reset

LCD_CAM_CAM_CONV_8BITS_DATA_INV Configures whether to swap every two bytes of input data.
O: Do not invert.
1: Invert.
(R/W)

LCD_CAM_CAM_CONV_YUV2YUV_MODE Configures the data format conversion in YUV-to-YUV mode.
O: Data is converted to YUV422 format.
1: Data is converted to YUV420 format.
2: Data is converted to YUV411 format.
3: Disabled.
Valid only when LCD_CAM_CAM_CONV_TRAN_MODE = 1.
(R/W)

LCD_CAM_CAM_CONV_YUV_MODE Configures the YUV format of the Camera input data in YUV-to-YUV mode or YUV-to-RGB mode.
O: Data is converted to YUV422 format.
1: Data is converted to YUV420 format.
2: Data is converted to YUV411 format.
(R/W)

LCD_CAM_CAM_CONV_PROTOCOL_MODE Configures the data format conversion standard.
O: BT601.
1: BT709.
(R/W)

LCD_CAM_CAM_CONV_DATA_OUT_MODE Configures the color range for the YUV-RGB converter's output data.
O: Limited color range.
1: Full color range.
(R/W)
```
Continued on the next page...
```