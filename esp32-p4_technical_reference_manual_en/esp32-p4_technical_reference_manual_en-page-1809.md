

```markdown
- the color range of RGB is: 16 ~ 240.
- the color range of YUV is:
    - Y: 16 ~ 240.
    - U-V: 16 ~ 235.

2. If the full color range is selected, the color range of RGB or YUV is 0 ~ 255.


## 38.3.7 LCD_CAM Timing

### 38.3.7.1 LCD Timing (RGB Format)

Figure 38.3-4 shows the LCD frame structure.

![Figure 38.3-4. LCD Frame Structure](image-placeholder)

As depicted in the figure, the frame structure can be set up with the following registers:

* `LCD_CAM_LCD_VT_HEIGHT`
* `LCD_CAM_LCD_VA_HEIGHT`
* `LCD_CAM_LCD_HB_FRONT`
* `LCD_CAM_LCD_HT_WIDTH`
* `LCD_CAM_LCD_HA_WIDTH`
* `LCD_CAM_VB_FRONT`

Figure 38.3-5 shows the timing of an LCD full frame.
```