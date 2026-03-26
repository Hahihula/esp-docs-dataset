

```markdown
Chapter 37 Pixel-Processing Accelerator (PPA)

Register 37.5. PPA_BLEND_COLOR_MODE_REG (0x0024)

Continued from the previous page...

PPA_BLENDO_RX_YUV_RANGE Configures the YUV range when the BLEND background input is YUV.
O: Limited range
1: Full range
(R/W)

PPA_BLEND_TX_YUV_RANGE Configures the YUV range when the BLEND output is YUV.
O: Limited range
1: Full range
(R/W)

PPA_BLENDO_RX_YUV2RGB_PROTOCOL Configures the YUV to RGB conversion protocol for the BLEND background input.
O: BT601
1: BT709
(R/W)

PPA_BLEND_TX_RGB2YUV_PROTOCOL Configures the YUV to RGB conversion protocol for the BLEND output.
O: BT601
1: BT709
(R/W)

PPA_BLENDO_RX_YUV422_BYTE_ORDER Configures the byte order when the BLEND background input is YUV422.
O: YVYU
1: YUYV
2: VYUY
3: UYVY
(R/W)
```