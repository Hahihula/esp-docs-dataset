

```markdown
Register 36.4. ISP_HSYNC_CNT_REG (0x0000)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 8   | ISP_HSYNC_CNT        |
| 7   | Reset               |

ISP_HSYNC_CNT Configures the interval between hsync and the previous vsync or line_end when converting Image Interface 32 data to ISP data. Generally, the default value is used. Measurement unit: Number of ISP_CLK clock cycles. (R/W)

Register 36.5. ISP_FRAME_CFG_REG (0x0010)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | (reserved)                      |
| 29  | ISP_HSYNC_END_EXIST             |
| 28  | ISP_HSYNC_START_EXIST           |
| 27  | [ISP_BAYER_MODE]                |
| 26  | (reserved)                      |
| 24  | ISP_HADR_NUM                    |
| 23  | ISP_VADR_NUM                    |
| 12  | 11                              |
| 0   | Reset                           |

ISP_VADR_NUM Configures the height of the input image, which should be set as the actual number of lines - 1. (R/W)

ISP_HADR_NUM Configures the width of the input image, which should be set as the actual width of lines - 1. (R/W)

ISP_BAYER_MODE Configures the Bayer mode of the input image.
0: BG/GR
1: GB/RG
2: GR/BG
3: RG/GB
(R/W)

ISP_HSYNC_START_EXIST Configures whether the hsync_start packet exists.
0: Not exist
1: Exist
(R/W)

ISP_HSYNC_END_EXIST Configures whether the hsync_end packet exists. This must have the same value as the ISP_HSYNC_START_EXIST field.
0: Not exist
1: Exist
(R/W)
```