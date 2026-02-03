Title: Chapter 29 LCD and Camera Controller (LCD_CAM)

Subtitle: Figure 29.4-2. LCD Timing (RGB Format)

Diagram Description:
The diagram shows the timing of a frame for an LCD display, with various signals labeled such as "LCD_VSYNC," "LCD_HSYNC," "LCD_DE," etc., along with annotations like "Timing of a frame" and "Timing of a line." There are also labels indicating different states: "Valid video data," "Invalid data."

Note:
"When configuring the parameters shown in the figures above, please note that the parameter is equal to the register value + 1. For example, if the expected VSYNC width is 1, then please configure LCD_CAM_LCD_VSYNC_WIDTH to 0. For more information, see the register description."

Steps (Listed as numbered instructions):
6. Set `LCD_CAM_LCD_UPDATE`.
7. Reset TX control unit (`LCD_Ctrl`) and Async Tx FIFO as described in Section 29.3.4.
8. Configure GDMA outlink.
9. Start transmitting data:
   - wait till LCD slave gets ready.
   - then set `LCD_CAM_LCD_START` to start transmitting data.

10. Wait for the interrupt signals set in Step 3.
11. In frame intervals during data transmitting, check if the bit `LCD_CAM_LCD_NXT FRAME_EN` is set:
    - If yes, set `LCD_CAM_LCD_UPDATE` (repeating the steps above) to continue transmitting next frame.
    - If not, LCD stops transmitting data.

12. Clear `LCD_CAM_LCD_START` if data transmission is done.

Subheading: 29.4.2 Configure LCD (I8080/MOTO6800 Format) as TX Mode

Body Text:
Figure 29.4-3 shows the LCD timing sequence in I8080 format.

Footer Information:
Espressif Systems
1088
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback