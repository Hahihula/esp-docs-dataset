**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**GoBack Link:** GoBack

**Section Heading:**
Configure the conversion mode:

**Table Title:**
Table 29.3-4. Conversion Mode Control

| Conversion Mode | TRANS_MODE | YUV_MODE | YUV2YUV_MODE |
|------------------|------------|----------|--------------|
| RGB565 → YUV422 | 1          | 0        | 3            |
| RGB565 → YUV420 | 1          | 1        | 3            |
| RGB565 → YUV411 | 1          | 2        | 3            |
| YUV422 → RGB565 | 0          | 0        | 3            |
| YUV420 → RGB565 | 0          | 1        | 3            |
| YUV411 → RGB565 | 0          | 2        | 3            |
| YUV422 → YUV420 | 1          | 0        | 1            |
| YUV422 → YUV411 | 1          | 1        | 2            |
| YUV420 → YUV422 | 1          | 1        | 0            |
| YUV420 → YUV411 | 1          | 1        | 2            |
| YUV411 → YUV422 | 1          | 2        | 0            |
| YUV411 → YUV420 | 1          | 2        | 1            |

**Footnotes:**
1. The value of LCD_CAM_LCD_CONVTransMode
2. The value of LCD_CAM_LCD_convYUV_mode
3. The value of LCD_CAM_LCD_convYUV2YUV_mode

**Instructions for Configuration (continued):**

- Configure the color range for input data by configuring LCD_CAM_LCD_CONVData_in_Mode:
  - full color range^1
  - limited color range^2
  
- Configure the color range for output data by configuring LCD_CAM_LCD_CONVData_out_Mode:
  - limited color range
  - full color range

**Note:**
1. If a full color range is selected, the color range of RGB or YUV is from 0 to 255.
2. For selecting an unlimited color range,
   - The color range for RGB will be between 16 and 240
   - The color range for YUV:
     - Y: Between 16 and 240
     - U-V: Between 16 and 235

**Section Heading (Next):**
29.4 Software Configuration Process

**Note in Section on Software Configuration Process:**

Updating the register configuration described in LCD module or camera module requires to set LCD_CAM_LCD_UPDATE and LCD_CAM_CAM_UPDATE, respectively, to synchronize registers from APB clock domain to LCD/camera clock do-...

**Footer Information:** 
Espressif Systems
1086 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback