

```markdown
Register 38.10. LCD_CAM_LCD_DLY_MODE_CFG1_REG (0x0030)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | LCD_CAM_LCD_VSYNC_MODE | LCD_CAM_LCD_HSYNC_MODE | LCD_CAM_LCD_DE_MODE | LCD_CAM_LCD_CD_MODE | LCD_CAM_DOUT23_MODE | LCD_CAM_DOUT22_MODE | LCD_CAM_DOUT21_MODE | LCD_CAM_DOUT20_MODE | LCD_CAM_DOUT19_MODE | LCD_CAM_DOUT18_MODE | LCD_CAM_DOUT17_MODE | LCD_CAM_DOUT16_MODE | Reset |
| Value | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 |

LCD_CAM_DOUTn_MODE (n: 16 - 23) Configures the delay of the output data bit (n).
- 0: No delay.
- 1: Delayed at the rising edge of LCD_CLK.
- 2: Delayed at the falling edge of LCD_CLK. (R/W)

LCD_CAM_LCD_CD_MODE Configures the delay of LCD_CD output signal.
- 0: No delay.
- 1: Delayed at the rising edge of LCD_CLK.
- 2: Delayed at the falling edge of LCD_CLK. (R/W)

LCD_CAM_LCD_DE_MODE Configures the delay of LCD_DE output signal.
- 0: No delay.
- 1: Delayed at the rising edge of LCD_CLK.
- 2: Delayed at the falling edge of LCD_CLK. (R/W)

LCD_CAM_LCD_HSYNC_MODE Configures the delay of LCD_HSYNC output signal.
- 0: No delay.
- 1: Delayed at the rising edge of LCD_CLK.
- 2: Delayed at the falling edge of LCD_CLK. (R/W)

LCD_CAM_LCD_VSYNC_MODE Configures the delay of LCD_VSYNC output signal.
- 0: No delay.
- 1: Delayed at the rising edge of LCD_CLK.
- 2: Delayed at the falling edge of LCD_CLK. (R/W)
```