**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Menu:**
GoBack

**Section Title:**
Register 29.12. LCD_CAM_CAM_CTRL1_REG (0x0008)

**Table Description:**
- The table shows the register bits with their corresponding descriptions.
- Bits are numbered from right to left, starting at bit '0' and ending at bit '31'.
- Each row describes a specific bit or group of bits in terms of functionality.

**Bit Descriptions (with explanations):**

- **LCD_CAM_CAM_AFI0_RESET**
  - LCD_CAM_CAM_AFI0_RESET
  - LCD_CAM_CAM_AFI0_RESET INV
  - LCD_CAM_CAM_AFI0 INV
  - LCD_CAM_CAM_AFI0 INV INV
  - LCD_CAM_CAM_AFI0 INV INV INV

- **LCD_CAM_CAM_START**
  - LCD_CAM_CAM_START
  - LCD_CAM_CAM_START INV
  - LCD_CAM_CAM_START INV INV
  - LCD_CAM_CAM_START INV INV INV

- ... (similar format for other bits)

**Detailed Descriptions:**

1. **LCD_CAM_CAM_REC_DATA_BYTELEN**
   - Configure camera received data byte length.
   - When the length of received data reaches this value + 1, GDMA_in_suc_eof_int is triggered.

2. **LCD_CAM_CAM_LINE_INT_NUM**
   - Configure line number.
   - When the number of received lines reaches this value + 1, LCD_CAM_CAM_HS_INT is triggered (R/W).

3. **LCD_CAM_CAM_CLK_INV_1**
   - Invert the input signal CAM_PCLK.

4. **LCD_CAM_VSYNC_FILTER_EN**
   - Enable CAM_VSYNC filter function.
   - 0: Bypass

5. **LCD_CAM_2BYTE_EN**
   - The width of input data is 16 bits (R/W).
   - 0: The width of input data is 8 bits.

6. **LCD_CAM_DE_INV**
   - CAM_DE invert enable signal, valid in high level.
   - R/W

7. **LCD_CAM_HSYNC INV**
   - CAM_HSYNC invert enable signal, valid in high level (R/W).

8. **CAM_VSYNC INV**
   - CAM_VSYNC invert enable signal.

9. **CAM_VH_DE_MODE_EN**
   - Input control signals are CAM_DE and CAM_HSYNC.
   - 1: CAM_VSYNC is enabled
   - 0: Input control signals are CAM_DE and CAM_VSYNC (R/W).

10. **CAM_DE INV**
    - CAM_DE invert enable signal, valid in high level.

11. **CAM_START**
    - Camera module start signal.
    - R/W

12. **CAM_RESET**
    - Camera module reset signal
    - WO

13. **CAM_AFI0_RESET**
    - Camera Async Rx FIFO reset signal (WO)

**Footer:**
Espressif Systems  
Page 1/1, Document Version ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback