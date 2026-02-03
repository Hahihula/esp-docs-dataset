**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Subtitles and Sections with Descriptions of Registers:**

1. **Register 29.16. LCD_CAM_LC_DMA_INT_ST_REG (0x006C)**
   - Description:
     ```
     LCD_CAM_LCD_VSYNC_IN_TST The status bit for LCD_CAM_LCD_VSYNC_IN_TST interrupt.
     LCD_CAM_LCDTrans_DONE_INT ST The status bit for LCD_CAM_LCDTrans_DONE_INT interrupt. (RO)
     LCD_CAM_CAM_VSYNC_IN_TST The status bit for LCD_CAM_CAM_VSYNC_IN_TST interrupt. (RO)
     LCD_CAM_CAM_HS_IN_TST The status bit for LCD_CAM_CAM_HS_IN_TST interrupt.
     ```
   - Binary Representation:
     ```
     0 0 0 0 0 0 0 0 0 0 0 0 0
     ```

2. **Register 29.17. LCD_CAM_LC_DMA_INR_CLR_REG (0x0070)**
   - Description:
     ```
     LCD_CAM_LCD_VSYNC_IN_TCLR The clear bit for LCD_CAM_LCD_VSYNC_IN_TST interrupt.
     LCD_CAM_LCDTrans_DONE_INT_CLR The clear bit for LCD_CAM_LCDTrans_DONE_INT interrupt. (WO)
     LCD_CAM_CAM_VSYNC_IN_TCLR The clear bit for LCD_CAM_CAM_VSYNC_IN_TST interrupt. (WO)
     LCD_CAM_CAM_HS_IN_TCLR The clear bit for LCD_CAM_CAM_HS_IN_TST interrupt.
     ```
   - Binary Representation:
     ```
     0 0 0 0 0 0 0 0 0 0 0 0
     ```

**Footer:**
Espressif Systems  
1104  
ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- GoBack
- Submit Documentation Feedback