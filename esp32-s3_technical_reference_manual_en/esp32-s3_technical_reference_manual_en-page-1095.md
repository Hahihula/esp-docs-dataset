**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**GoBack Link:** GoBack

---

**Register Section Header:**
Register 29.3. LCD_CAM_LCD_USER_REG (0x014)

**Table Description:**
- The table lists various registers related to the LCD_CAM module, with their bit positions ranging from bits 31 down to bits 0.
- Each register is labeled and has a description of its function.

---

**Register Descriptions in Markdown Format:**

- **LCD_CAM_LCD_DOUT_CYCLELEN:** Configure the cycles for DOUT phase of LCD module. The cycles = this value + 1. (R/W)
  
- **LCD_CAM_LCD_ALWAYS_OUT_EN:** LCD continues outputting data when LCD is in DOUT phase, till LCD_CAM_LCD_START is cleared or LCD_CAM_LCD_RESET is set. (R/W)

- **LCD_CAM_LCD_8BITS_ORDER:** Swap every two data bytes, valid in 8-bit mode.
   - Value: `0`: Do not swap
   - Access Type: Read/Write

- **LCD_CAM_LCD_UPDATE:** Update LCD registers. This bit is cleared by hardware.
   - Value: `0`: Do not care
   - Access Type: Read/Write

- **LCD_CAM_LCD_BIT_ORDER:** Change data bit order, change LCD_DATA_out[7:0] to LCD_DATA_out[0:7] in 8-bit mode and bits[15:0] to bits[0:15] in 16-bit mode.
   - Value: `0`: Do not change
   - Access Type: Read/Write

- **LCD_CAM_LCD_BYTE_ORDER:** Invert data byte order, only valid in 16-bit mode. 
   - Value: `0`: Do not invert
   - Access Type: Read/Write

- **LCD_CAM_LCD_2BYTE_EN:** The width of output LCD data is 16 bits.
   - Description: The width of output LCD data is 8 bits (R/W)

- **LCD_CAM_LCD_DOUT:** Be able to send data out in LCD sequence when LCD starts. 
   - Value: `0`: Disable
   - Access Type: Read/Write

- **LCD_CAM_LCDDummy:** Enable DUMMY phase in LCD sequence when LCD starts.
   - Description: Disable (R/W)

- **LCD_CAM_LCD_CMD:** Be able to send command in LCD sequence when LCD starts. 
   - Value: `0`: Disable
   - Access Type: Read/Write

- **LCD_CAM_LCD_START:** LCD starts sending data enable signal, valid in high level.
   - Description: (R/W)

- **LCD_CAM_LCD_RESET:** Reset LCD module.
   - Value: `(WO)`
   - Description: Write Only

- **LCD_CAM_LCDDummy_CYCLELEN:** Configure DUMMY cycles. DUMMY cycles = this value + 1
   - Access Type: Read/Write

- **LCD_CAM_LCD_CMD_2_CYCLE_EN:** The cycle length of command phase.
   - Value: `1`: 2 cycles, `0`: 1 cycle (R/W)

---

**Footer Information:**
Espressif Systems  
Page Number: 1095  
Document Title: ESP32-S3 TRM (Version 1.7)  
Feedback Link: Submit Documentation Feedback