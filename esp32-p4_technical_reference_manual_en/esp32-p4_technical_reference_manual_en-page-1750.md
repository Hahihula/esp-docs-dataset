

```markdown
Register 36.158. CSI_BRIG_HOST_CM_CTRL_REG (0x0048)

Continued from the previous page...

CSI_BRIG_CSI_HOST_CM_RX_YUV422_FORMAT Configures the channel order of input YUV422 data.
O: YVYU
1: YUYV
2: VYUY
3: UYVY
(R/W)

CSI_BRIG_CSI_HOST_CM_CTX Configures the output image format of CSI CM.
O: RGB888
1: RGB565
2: YUV422
3: YUV420
(R/W)

CSI_BRIG_CSI_HOST_CM_LANE_NUM Configures the number of CSI channels; valid only when both input and output formats are RGB888.
O: 1 channel
1: 2 channels
(R/W)

CSI_BRIG_CSI_HOST_CM_16BIT_SWAP Configures whether to enable 16-bit high/low swapping.
O: Disable
1: Enable
(R/W)

CSI_BRIG_CSI_HOST_CM_8BIT_SWAP Configures whether to enable 8-bit high/low swapping.
O: Disable
1: Enable
(R/W)
```