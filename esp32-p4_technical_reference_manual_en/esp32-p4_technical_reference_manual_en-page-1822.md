

```markdown
Register 38.7. LCD_CAM_LCD_CTRL2_REG (0x0024)

| 31 | 24 | 23 | 22 | 16 | 15 | 10 | 9 | 8 | 7 | 6 | 1 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|---|
|    | LCD_CAM_LCD_HSYNC_POSITION | LCD_CAM_LCD_HSYNC_IDLE_POL | LCD_CAM_LCD_HSYNC_WIDTH | (reserved) | LCD_CAM_LCD_HS_BLANK_EN | LCD_CAM_LCD_DE_IDLE_POL | LCD_CAM_LCD_VSYNC_IDLE_POL | Reset |

LCD_CAM_LCD_VSYNC_WIDTH Configures the width of LCD_VSYNC active pulse in a line. Expected
width = this value + 1. (R/W)

LCD_CAM_LCD_VSYNC_IDLE_POL Configures the idle value of LCD_VSYNC.
0: The idle value is low.
1: The idle value is high.
(R/W)

LCD_CAM_LCD_DE_IDLE_POL Configures the idle value of LCD_DE.
0: The idle value is low.
1: The idle value is high.
(R/W)

LCD_CAM_LCD_HS_BLANK_EN Configures the LCD_HSYNC output in RGB mode.
0: LCD_HSYNC is output only in active video lines.
1: LCD_HSYNC can be output in vertical blanking intervals.
(R/W)

LCD_CAM_LCD_HSYNC_WIDTH Configures the width of LCD_HSYNC active pulse. Expected width
= this value +1. (R/W)

LCD_CAM_LCD_HSYNC_IDLE_POL Configures the idle value of LCD_HSYNC.
0: The idle value is low.
1: The idle value is high.
(R/W)

LCD_CAM_LCD_HSYNC_POSITION Configures the position of LCD_HSYNC active pulse. Expected
position = this value + 1. Unit is a pixel. (R/W)
```