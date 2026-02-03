**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Header:**
Register 29.4. LCD_CAM_LCD_MISC_REG (0x018)

**Table Header:**
- LCD_CAM_LCD_IDLE_EDGE
- LCD_CAM_LCD_DUMMY_SET
- LCD_CAM_LCD_DATA_RESET
- LCD_CAM_LCD_AFIRO_BK_EN
- LCD_CAM_LCD_VBK_CYCLELEN
- LCD_CAM_LCD_VFK_CYCLELEN

**Binary Representation Table:**
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 12 | 11 | 10 | 9 |
|----|----|----|----|----|----|----|----|----|----|----|--|
|     |     |     |     |     |     |     |     |     |     |     | Reset |

**Description:**
- **LCD_CAM_LCD_AFIHO_THRESHOLD_NUM**: Set the threshold for Async Tx FIFO full event. (R/W)
  - LCD_CAM_LCD_VFK_CYCLELEN
    - Configure the setup cycles in LCD non-RGB mode. Setup cycles expected = this value + 1. (R/W)

- **LCD_CAM_LCD_VBK_CYCLELEN**
  - Configure the hold time cycles in LCD non-RGB mode. Hold cycles expected = this value + 1. (R/W)

- **LCD_CAM_LCD_NEXT_FRAME_EN**
  - Send the next frame data when the current frame is sent out.
    - O: LCD stops when the current frame is sent out. (R/W)
    - 1: Enable blank region when LCD sends data out.

- **LCD_CAM_LCD_AFIHO_RESET**
  - Async Tx FIFO reset signal. (WO)

- **LCD_CAM_LCD_CD_DATA_SET**
  - LCD_CD = !LCD_CAM_LCD_IDLE_EDGE when LCD is in DOUT phase.
    - O: LCD_CD = LCD_CAM_LCD_IDLE_EDGE. (R/W)
    - 1: LCD_CD = !LCD_CAM_LCD_IDLE_EDGE

- **LCD_CAM_LCD_CD_DUMMY_SET**
  - LCD_CD = !LCD_CAM_LCD_IDLE_EDGE when LCD is in DUMMY phase.

- **LCD_CAM_LCD_CD_CMD_SET**
  - LCD_CD = !LCD_CAM_LCD_IDLE_EDGE when LCD is in CMD phase.
    - O: LCD_CD = LCD_CAM_LCD_IDLE_EDGE. (R/W)

- **LCD_CAM_LCD_CD_IDLE_EDGE**
  - The default value of LCD_CD.

**Footer Information:**
Espressif Systems
Page number: 1096

**Document Version and Feedback Link:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback