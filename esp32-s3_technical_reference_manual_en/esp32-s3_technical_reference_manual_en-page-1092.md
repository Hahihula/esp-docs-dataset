**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Subtitle:**
29.6 Register Summary

**Body Text:**
The addresses in this section are relative to LCD_CAM controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

1. **LCD configuration registers**
   - LCD_CAM_LCD_CLOCK_REG
     - LCD clock configuration register
     - 0x0000 R/W
   - LCD_CAM_LCD_RGB_YUV_REG
     - LCD data format conversion register
     - 0x0010 R/W

2. **Interrupt registers**
   - LCD_CAM_LC_DMA_INT_ENA_REG
     - LCD_CAM GDMA interrupt enable register
     - 0x0064 R/W
   - LCD_CAM_LC_DMA_INT_RAW_REG
     - LCD_CAM GDMA raw interrupt status register
     - 0x0068 RO

3. **Version register**
   - LCD_CAM_LC_REG_DATE_REG
     - Version control register
     - 0x00FC R/W

**Footer:**
Espressif Systems  
1092 ESP32-S3 TRM (Version 1.7)