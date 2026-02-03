**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Body Text:**

- If YUV-RGB format conversion is used meanwhile, the pixel clock frequency must be less than 60 MHz.
  
- **If 16-bit parallel data input mode is selected**, then:
  - Pixel clock frequency must be less than 40 MHz.

- *if YUV-RGB format conversion is used meanwhile, the pixel clock frequency must be less than 30 MHz.*

- If an external camera and an external LCD are connected simultaneously, ensure that the maximum data throughput on the interface is less than GDMA total data bandwidth of 80 MB/s. Note the default frequency of APB_CLK is 80 MHz here. For more information, see Chapter 7 Reset and Clock.

**Subtitle:**
29.5 LCD_CAM Interrupts

**List (Bullet Points):**

- **LCD_CAM_CAM_HS_IN**: triggered when the total number of received lines by camera is greater than or equal to LCD_CAM_CAM_LINE_INT_NUM + 1.
  
- **LCD_CAM_CAM_VSYNC_IN**: triggered when the camera received a VSYNC signal.

- **LCD_CAM_LCDCTrans_DONE_IN**: triggered when the LCD transmitted all the data.

- **LCD_CAM_LCDC_VSYNC_IN**: triggered when the LCD transmitted a VSYNC signal. 

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:** 
1091 ESP32-S3 TRM (Version 1.7)