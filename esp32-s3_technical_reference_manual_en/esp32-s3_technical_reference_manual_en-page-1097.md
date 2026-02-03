**Chapter Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Number**: Register 29.5, LCD_CAM_LCD_CTRL_REG (0x001C)
  - **Field Descriptions**:
    - `LCD_CAM_LCD_RBG_MODE_EN`
      - Description: Configures the value of (HSYNC_POSITION + HSYNC_WIDTH + horizontal back porch). (R/W)

    - `LCD_CAM_LCD_VA_HEIGHT`
      - Description: It is the vertical active height of a frame. (R/W)

    - `LCD_CAM_LCD_VI_HEIGHT`
      - Description: It is the vertical total height of a frame. (R/W)

    - `LCD_CAM_LCD_RGB_MODE_EN`
      - Description: Enable RGB mode, and input VSYNC, HSYNC, and DE signals.
        - 0: Disable. (R/W)

---

**Register Section Header:**

- **Register Number**: Register 29.6, LCD_CAM_LCD_CTRL1_REG (0x020)
  - **Field Descriptions**:
    - `LCD_CAM_LCD_VB_FRONT`
      - Description: Configures the value of (VSYNC_WIDTH + vertical back porch). (R/W)

    - `LCD_CAM_LCD_HA_WIDTH`
      - Description: It is the horizontal active width of a frame. (R/W)

    - `LCD_CAM_LCD_HT_WIDTH`
      - Description: It is the horizontal total width of a frame. (R/W)

---

**Footer Information:** 
- **Company**: Espressif Systems
- **Page Number**: 1097
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Links**: Submit Documentation Feedback