

```markdown
Register 6.7. DMA2D_OUT_COLOR_CONVERT_CHn_REG (n: 0-3) (0x0048+0x100*n)

DMA2D_OUT_COLOR_OUTPUT_SEL_CHn   Configures the third stage output of color space conversion for TX channel n.
O: RGB888 to RGB565
1: YUV444 to YUV422
2: Output directly
Others: Invalid
(R/W)

DMA2D_OUT_COLOR_3B_PROC_EN_CHn   Configures whether to enable the second stage of color space conversion for TX channel n.
O: Disable
1: Enable
(R/W)

DMA2D_OUT_COLOR_INPUT_SEL_CHn    Configures the first stage output of color space conversion for TX channel n.
O: RGB565 to RGB888
1: YUV422 to YUV444
2: Other 2 bytes/pixel color format
3: Other 3 bytes/pixel color format
7: Disable color space conversion
Others: Invalid
(R/W)
```