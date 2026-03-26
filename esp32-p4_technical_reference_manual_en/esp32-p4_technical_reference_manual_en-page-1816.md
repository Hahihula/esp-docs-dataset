

```markdown
|Bit|31|30|29|28|27|26|25|24|23|22|21|20|19|18|17|
|:---------------------------------------------|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Value|0| | | | | | | |3| | | | | |
|| ||||||||0|3| ||
||(reserved)||||||||||||||||
||LCD_CAM_LCD_CONV_RGB2RGB_MODE|Configures data format conversion in RGB-to-RGB mode.|
|O: Data is converted to RGB565 format.|1: Data is converted to RGB888 format.|2/3: Data format conversion is disabled. (R/W)|
|LCD_CAM_LCD_CONV_8BITS_DATA_INV|Configures whether to swap every two 8-bit GDMA input data.|
|O: Do not swap.|1: Swap. (R/W)|
|LCD_CAM_LCD_CONV_YUV2YUV_MODE|Configures data format conversion in YUV-to-YUV mode.|
|O: Data is converted to YUV422 format.|1: Data is converted to YUV420 format.|2: Data is converted to YUV411 format.|3: Data format conversion is disabled. Only valid when LCD_CAM_LCD_CONV_TRAN_MODE = 1. (R/W)|
|LCD_CAM_LCD_CONV_YUV_MODE|Configures the YUV format of input data in YUV-to-YUV mode and YUV-to-RGB mode.|
|O: Input data is in YUV422 format.|1: Input data is in YUV420 format.|2: Input data is in YUV411 format. (R/W)|
|LCD_CAM_LCD_CONV_PROTOCOL_MODE|Configures the data format conversion standard.|
|O: BT601.|1: BT709. (R/W)|
|LCD_CAM_LCD_CONV_DATA_OUT_MODE|Configures the color range for output data.|
|O: Limited color range.|1: Full color range. (R/W)|
```