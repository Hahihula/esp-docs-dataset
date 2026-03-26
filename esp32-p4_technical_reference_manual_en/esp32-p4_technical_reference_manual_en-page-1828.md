

```markdown
Chapter 38 LCD and Camera Controller (LCD_CAM)

Register 38.13. LCD_CAM_CAM_CTRL1_REG (0x0008)

Continued from the previous page...

LCD_CAM_CAM_VH_DE_MODE_EN Configures the input control signals.
    0: VSYNC and DE signals control the data. In this case, wiring HSYNC signal line is not a must.
        But in this case, the YUV-RGB conversion function of the camera module is not available.
    1: VSYNC, HSYNC, and DE signals control the data. In this case, users need to wire the three
        signal lines.
        (R/W)

LCD_CAM_CAM_START Camera module start signal. (R/W)

LCD_CAM_CAM_RESET When set to 1, the Camera module is reset. (WO)

LCD_CAM_CAM_AFIFO_RESET When set to 1, the Camera Async RX FIFO is reset. (WO)
```