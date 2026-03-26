

```markdown
Table 38.3-5. Conversion Mode Control in 24-bit Mode

| Conversion Mode | TRANS_MODE¹ | YUV_MODE² | YUV2YUV_MODE³ | RGB2RGB_MODE⁴ |
|-----------------|-------------|-----------|---------------|---------------|
| RGB565 → YUV444 | 1           | -         | 3             | -             |
| RGB565 → RGB888 | 0           | -         | -             | 1             |
| YUV422 → RGB888 | 0           | 0         | 3             | -             |
| YUV411 → RGB888 | 0           | 2         | 3             | -             |
| YUV422 → YUV444 | 1           | 0         | 0/1/2         | -             |
| YUV411 → YUV444 | 1           | 2         | 0/1/2         | -             |

¹ The value of `LCD_CAM_LCD_CONV_TRANS_MODE`
² The value of `LCD_CAM_LCD_CONV_YUV_MODE`
³ The value of `LCD_CAM_LCD_CONV_YUV2YUV_MODE`
⁴ The value of `LCD_CAM_LCD_CONV_RGB2RGB_MODE`

• In other output modes:

Table 38.3-6. Conversion Mode Control in Other Modes

| Conversion Mode | TRANS_MODE¹ | YUV_MODE² | YUV2YUV_MODE³ | RGB2RGB_MODE⁴ |
|-----------------|-------------|-----------|---------------|---------------|
| RGB565 → YUV422 | 1           | 0         | 3             | -             |
| RGB565 → YUV420 | 1           | 1         | 3             | -             |
| RGB565 → YUV411 | 1           | 2         | 3             | -             |
| RGB888 → RGB565 | 0           | -         | -             | 1             |
| YUV422 → RGB565 | 0           | 0         | 3             | -             |
| YUV411 → RGB565 | 0           | 2         | 3             | -             |
| YUV422 → YUV420 | 1           | 0         | 1             | -             |
| YUV422 → YUV411 | 1           | 0         | 2             | -             |
| YUV411 → YUV422 | 1           | 2         | 0             | -             |
| YUV411 → YUV420 | 1           | 2         | 1             | -             |

¹ The value of `LCD_CAM_LCD_CONV_TRANS_MODE`
² The value of `LCD_CAM_LCD_CONV_YUV_MODE`
³ The value of `LCD_CAM_LCD_CONV_YUV2YUV_MODE`
⁴ The value of `LCD_CAM_LCD_CONV_RGB2RGB_MODE`

6. Configure the color range for the input data by configuring `LCD_CAM_LCD_CONV_DATA_IN_MODE`:
  • 0: limited color range¹
  • 1: full color range²

7. Configure the color range for the output data by configuring `LCD_CAM_LCD_CONV_DATA_OUT_MODE`:
  • 0: limited color range¹
  • 1: full color range²

Note:
1. If the limited color range is selected,
```