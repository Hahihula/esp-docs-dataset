**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Back Link:**
GoBack

**Subtitle:**
Register 29.11. LCD_CAM_CAM_CTRL_REG (0x004)

**Table Description:**
- The table lists various registers related to the LCD_CAM controller, including their bit positions in a byte and descriptions of what each register does.

**Text Entries from Table with Descriptions:**

- **LCD_CAM_CAM_STOP_EN:** Camera stop enable signal. 1: camera stops when GDMA Rx FIFO is full.
  - Value Range (0x0): Do not stop. (R/W)

- **LCD_CAM_CAM_VSYNC_FILTER_THRES:** Filter threshold value for CAM_VSYNC signal.
  - Description: (R/W)
  
- **LCD_CAM_CAM_UPDATE:** Update camera registers. This bit is cleared by hardware.
  - Value Range (0x0): Do not care. (R/W)

- **LCD_CAM_CAM_BYTE_ORDER:** Invert data byte order, only valid in 16-bit mode.
  - Description: Change data byte order; do not change the value of CAM_DATA_in[7:0] to CAM_DATA_in[0:7].
  - Value Range (0x0): Do not care. (R/W)

- **LCD_CAM_CAM_BIT_ORDER:** Change data bit order, changing CAM_DATA_in[7:0] in 8-bit mode and bits[15:0] to bits[0:15] in 16-bit mode.
  - Description: Enable or disable the generation of LCD_CAM_CAM_HS_INT.
  - Value Range (0x0): Do not care. (R/W)

- **LCD_CAM_CAM_VS_EOF_EN:** Enable CAM_VSYNC to generate in_suc_eof; 0: in_suc_eof is controlled by LCD_CAM_CAM_REC_DATA BYTELEN.
  - Description: (R/W)
  
- **LCD_CAM_CAM_CLKM_DIV_NUM:** Integral camera clock divider value. 
  - Value Range (0x0): Do not care.

- **LCD_CAM_CAM_CLKM_DIV_B:** Fractional clock divider numerator value, which is a fraction of the integral clock.
  - Description: (R/W)

- **LCD_CAM_CAM_CLKM_DIV_A:** Fractional clock divider denominator value. 
  - Value Range (0x0): Do not care.

- **LCD_CAM_CAM_CLKM_SEL:** Select camera module source clock; 0: Clock source is disabled, 1: XTAL_CLK.
  - Description:
    - XTAL_CLK.2: PLL_D2_CLK
    - XTAL_CLK.3: PLL_F160M_CLK

**Footer Information:**
- Page number and document version information at the bottom of the page.

**Company Name:** 
Espressif Systems 

**Document Version Note:**
ESP32-S3 TRM (Version 1.7)