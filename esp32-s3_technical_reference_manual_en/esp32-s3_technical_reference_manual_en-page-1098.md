**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Back Link:**
GoBack

**Register Section Header:**
Register 29.7. LCD_CAM_LCD_CTRL2_REG (0x024)

**Binary Register Diagram Description with Labels for Each Bit Position from Left to Right, Top Row to Bottom Row:**
- LCD_CAM_LCD_HSYNC_POSITION
- LCD_CAM_LCD_HSYNC_IDLE Пол
- LCD_CAM_LCD_VSYNC_WIDTH
- LCD_CAM_LCD_DE_IDLE Пол

**Register Details and Descriptions in Markdown Format:**

1. **LCD_CAM_LCD_VSYNC_WIDTH**: 
   - Description: It is the width of LCD_VSYNC active pulse in a line.
   - Access Type (R/W): Read/Write
   
2. **LCD_CAM_LCD_VSYNC_IDLE_POL**:
   - Description: It is the idle value of LCD_VSYNC.
   - Access Type (R/W): Read/Write

3. **LCD_CAM_LCD_DE_IDLE Пол**:
   - Description: It is the idle value of LCD_DE.
   - Access Type (R/W): Read/Write

4. **LCD_CAM_LCD_HS_BLANK_EN**:
   - Description: The pulse of LCD_HSYNC is out in vertical blanking lines in RGB mode, 0: LCD_HSYNC pulse valid only active region lines in RGB mode
   - Access Type (R/W): Read/Write

5. **LCD_CAM_LCD_HSYNC_WIDTH**:
   - Description: Configures the width of LCD_HSYNC active pulse.
   - Expected Width = this value +1.

6. **LCD_CAM_LCD_HSYNC_IDLE Пол**:
   - Description: It is the idle value of LCD_HSsync
   - Access Type (R/W): Read/Write

7. **LCD_CAM_LCD_HSYNC_POSITION**:
   - Description: Configures the position of LCD_HSsync active pulse.
   - Expected Position = this value +1, Unit in pixel.

**Register Section Header for Another Register:**
Register 29.8. LCD_CAM_LCD_CMD_VAL_REG (0x0028)

**Binary Register Diagram Description with Labels for Each Bit Position from Left to Right:
- LCD_CAM_LCD_CMD_VALUE

**Register Details and Descriptions in Markdown Format:

1. **LCD_CAM_LCD_CMD_VALUE**:
   - Description: The LCD write command value.
   - Access Type (R/W): Read/Write

**Footer Information:**
Espressif Systems
Page Number 1098
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback