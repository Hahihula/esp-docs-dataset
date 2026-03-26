

```markdown
Register 38.5. LCD_CAM_LCD_CTRL_REG (0x001C)

| 31 | 30           | 21   | 20         | 11       | 10          | Reset |
|----|--------------|------|------------|----------|-------------|-------|
|    | LCD_CAM_LCD_RGB_MODE_EN |      | LCD_CAM_LCD_VI_HEIGHT |          |             |       |

LCD_CAM_LCD_HB_FRONT Configures the value of (HSYNC_POSITION + HSYNC_WIDTH + horizontal back porch). (R/W)

LCD_CAM_LCD_VA_HEIGHT Configures the vertical active height of a frame. (R/W)

LCD_CAM_LCD_VI_HEIGHT Configures the vertical total height of a frame. (R/W)

LCD_CAM_LCD_RGB_MODE_EN Configures whether to enable RGB mode.
  0: Disable RGB mode.
  1: Enable RGB mode and input VSYNC, HSYNC, and DE signals.
(R/W)
```

```markdown
Register 38.6. LCD_CAM_LCD_CTRL1_REG (0x0020)

| 31 | 20   | 19         | 8          | 7        | Reset |
|----|------|------------|------------|----------|-------|
|    |      | LCD_CAM_LCD_HT_WIDTH |            |          |       |

LCD_CAM_LCD_VB_FRONT Configures the value of (VSYNC_WIDTH + vertical back porch). (R/W)

LCD_CAM_LCD_HA_WIDTH Configures the horizontal active width of a frame. (R/W)

LCD_CAM_LCD_HT_WIDTH Configures the horizontal total width of a frame. (R/W)
```