

```markdown
Chapter 37 Pixel-Processing Accelerator (PPA) GoBack


Register 37.5. PPA_BLEND_COLOR_MODE_REG (0x0024)

PPA_BLEND0_RX_YUV422_BYTE_ORDER
PPA_BLEND0_RX_RGB2YUV_PROTOCAL
PPA_BLEND0_RX_TX_YUV_RANGE
PPA_BLEND1_RX_CM
PPA_BLEND0_RX_CM

31 18 17 16 15 14 13 12 11 8 7 4 3 0
+-----------------------------+
| 0 0 0 0 0 0 0 0 0 0 O O O | Reset
+-----------------------------+

PPA_BLENDO_RX_CM Configures the input image color format for BLEND background layer.
O: ARGB8888
1: RGB888
2: RGB565
4: L8
5: L4
8: YUV420
9: YUV422
12: GRAY
Others: Reserved
(R/W)

PPA_BLEND1_RX_CM Configures the input image color format for BLEND foreground layer.
O: ARGB8888
1: RGB888
2: RGB565
4: L8
5: L4
6: A8
7: A4
Others: Reserved
(R/W)

PPA_BLEND_TX_CM Configures the output image color format of BLEND.
O: ARGB8888
1: RGB888
2: RGB565
8: YUV420
9: YUV422
12: GRAY
Others: Reserved
(R/W)

Continued on the next page...
```