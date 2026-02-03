**Title:**
Chapter 29 LCD and Camera Controller (LCD_CAM)

**Diagram Description:**
Figure 29.4-3 shows an "LCD Timing (I8080 Format)" with labels for various signals such as LCD_CS, LCD_DC, LCD_PCLK, LCD_Data_out[15:0], CMD, DUMMY state, Data_0 to Data_n.

**Body Text and Instructions:**

Follow the steps below to configure LCD (I8080 format) as TX mode via software:

1. Configure clock according to Section 29.3.3.
2. Configure signal pins according to Table 29.3-1.
3. Enable corresponding interrupts, see Section 29.5.

4. Clear `LCD_CAM_LCD_RGB_MODE_EN`.
5. Configure CMD phase by LCD_CAM_LCD_CMD, LCD_CAM_LCD_CMD_2_CYCLE_EN, and LCD_CAM_LCD_CMD_VALUE.
6. Configure DUMMY phase by LCD_CAM_LCD_DUMMY and LCD_CAM_LCD_DUMMY_CYCLELEN.
7. Configure DOUT phase by LCD_CAM_LCD_DOUT, depending on the output mode:
   - In a fixed-length output^a, configure data length in LCD_CAM_LCD_DOUT_CYCLELEN.
   - In a continuous output^b, set LCD_CAM_LCD_ALWAYS_OUT_EN. Users do not need to configure LCD_CAM_LCD_DOUT_CYCLELEN.

**Note:**
(a) In a fixed-length output, the LCD module stops sending data once the data length reaches the value set in `LCD_CAM_LCD_DOUT_CYCLELEN`.
(b) In a continuous output, LCD module keeps sending data till:
   - LCD_CAM_LCD_START is cleared;
   - or LCD_CAM_LCD_RESET is set;
   - or all the data in GDMA is sent out.

8. Configure the CD signal mode, including the default value of the CD signal and the values at each phase; see the description of `LCD_CAM_LCD_MISG_REG`.
9. Set `LCD_CAM_LCD_UPDATE`.
10. Reset TX control unit (LCD_Ctrl) and Async Tx FIFO as described in Section 29.3.4.
11. Configure GDMA outlink.
12. Start transmitting data:
    - wait till LCD slave gets ready.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)