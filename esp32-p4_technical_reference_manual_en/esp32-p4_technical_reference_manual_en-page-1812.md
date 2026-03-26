

```markdown
2. Configure signal pins according to Table 38.3-1 and Chapter 9 GPIO Matrix and IO MUX.
3. Enable corresponding interrupts, see Section 38.4.
4. Clear LCD_CAM_LCD_RGB_MODE_EN to disable RGB format.
5. Configure CMD phase with LCD_CAM_LCD_CMD, LCD_CAM_LCD_CMD_2_CYCLE_EN, and LCD_CAM_LCD_LATTER_CMD_VALUE.
6. Configure DUMMY phase with LCD_CAM_LCD_DUMMY and LCD_CAM_LCD_DUMMY_CYCLELEN.
7. Configure DOUT phase with LCD_CAM_LCD_DOUT, depending on the output mode:

- In a fixed-length output¹, configure data length in LCD_CAM_LCD_DOUT_CYCLELEN.
- In a continuous output², set LCD_CAM_LCD_ALWAYS_OUT_EN. Users do not need to configure LCD_CAM_LCD_DOUT_CYCLELEN.

Note:
(a) In a fixed-length output, the LCD module stops sending data once the data length reaches the value set in LCD_CAM_LCD_DOUT_CYCLELEN.
(b) In a continuous output, LCD module keeps sending data till:
    - LCD_CAM_LCD_START is cleared;
    - or LCD_CAM_LCD_RESET is set;
    - or all the data in GDMA is sent out.

8. Configure the CD signal mode, including the default value of the CD signal and the values at each phase, see the description of LCD_CAM_LCD_MISC_REG.
9. Set LCD_CAM_LCD_UPDATE so that the configurations take effect.
10. Reset TX control unit (LCD_Ctrl) and Async TX FIFO as described in Section 38.3.4.
11. Configure GDMA outlink, see Chapter 5 VDMA Controller (VDMA).
12. Start transmitting data:

- Wait till LCD slave gets ready.
- Set LCD_CAM_LCD_START to start transmitting data.

13. Wait for the interrupt signals set in Step 2.
14. Clear LCD_CAM_LCD_START if data transmission is done.

Notes:
No matter in which format, RGB or I8080/MOTO6800, the rules below must be followed when accessing internal and external memory via GDMA:

- If LCD data bus is configured to 8-bit parallel output mode, then
    - The pixel clock frequency must be less than 80 MHz.
        - If YUV-RGB format conversion is being used at the same time, the pixel clock frequency must be less than 60 MHz.
- If LCD data bus is configured to 16-bit parallel output mode, then
```