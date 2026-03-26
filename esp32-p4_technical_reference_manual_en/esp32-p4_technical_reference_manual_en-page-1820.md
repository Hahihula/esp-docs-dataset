

```markdown
Register 38.4. LCD_CAM_LCD_MISC_REG (0x0018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 12 | 11 | 6 | 5 | 4 | 3 | Reset |
|-----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|--------|
|     | 0  | 0  | 0  | 0  | 0  | 0  |    |    | 0x00 | 0x3 | 0 | 0 | 0 | 0 |        |

LCD_CAM_LCD_WIRE_MODE Configures the bit width of LCD output data to GPIO.
0: 8-bit
1: 16-bit
2: 24-bit
(R/W)

LCD_CAM_LCD_VFK_CYCLELEN Configures the clock cycles of the setup time in LCD non-RGB mode. Setup clock cycles = this value + 1. (R/W)

LCD_CAM_LCD_VBK_CYCLELEN Configures the clock cycles of the hold time in LCD non-RGB mode. Hold clock cycles = this value + 1. (R/W)

LCD_CAM_LCD_NEXT_FRAME_EN Configures whether to send the next frame.
0: The LCD module stops when the current frame is sent out.
1: The LCD module continues sending the next frame when the current frame is sent out.
(R/W)

LCD_CAM_LCD_BK_EN Configures whether to enable blanking region when LCD sends data.
0: No blanking region.
1: Enable blanking region.
(R/W)

LCD_CAM_LCD_AFIFO_RESET When set to 1, Async TX FIFO is reset. (WO)

LCD_CAM_LCD_CD_DATA_SET Configures LCD_CD value in DOUT phase for LCD I8080 mode.
0: LCD_CD = LCD_CAM_LCD_CD_IDLE_EDGE
1: LCD_CD = !LCD_CAM_LCD_CD_IDLE_EDGE
(R/W)

LCD_CAM_LCD_CD_DUMMY_SET Configures LCD_CD value in DUMMY phase for LCD I8080 mode.
0: LCD_CD = LCD_CAM_LCD_CD_IDLE_EDGE
1: LCD_CD = !LCD_CAM_LCD_CD_IDLE_EDGE
(R/W)

LCD_CAM_LCD_CD_CMD_SET Configures LCD_CD value in CMD phase for LCD I8080 mode.
0: LCD_CD = LCD_CAM_LCD_CD_IDLE_EDGE
1: LCD_CD = !LCD_CAM_LCD_CD_IDLE_EDGE
(R/W)

LCD_CAM_LCD_CD_IDLE_EDGE The default value of LCD_CD. (R/W)
```