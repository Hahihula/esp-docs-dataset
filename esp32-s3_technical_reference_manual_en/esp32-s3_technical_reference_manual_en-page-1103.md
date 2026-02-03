**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Subtitles and Sections:**

1. **Register 29.14. LCD_CAM_LC_DMA_INT_ENA_REG (0x0064)**
   - **Field Description:** 
     - `LCD_CAM_LCD_VSYNC_INTENA`: The enable bit for LCD_CAM_LCD_VSYNC_INTE interrupt.
     - `LCD_CAM_LCDTransDoneIntENA`: The enable bit for LCD_CAM_LCD_Trans_Done_INT_in-errupt. (R/W)
     - `LCD_CAM_CAM_VSYNC_INTENA`: The enable bit for LCD_CAM_CAM_VSYNC_INTE interrupt.

2. **Register 29.15. LCD_CAM_LC_DMA_INT_RAW_REG (0x0068)**
   - **Field Description:**
     - `LCD_CAM_LCD_VSYNC_INTRAW`: The raw bit for LCD_CAM_LCD_VSYNC_INTE interrupt.
     - `LCD_CAM_LCDTransDoneIntRAW`: The raw bit for LCD_CAM_LCD_Trans_Done_INT_inter-rupt. (RO)
     - `LCD_CAM_CAM_VSYNC_INTRAW`: The raw bit for LCD_CAM_CAM_VSYNC_INTE interrupt.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)