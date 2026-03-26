

```markdown
Register 36.158. CSI_BRIG_HOST_CM_CTRL_REG (0x0048)

| Bit | Field Name | Description |
|-----|------------|-------------|
| 31  |            | (reserved)  |
| 30  |            |             |
| 29  |            |             |
| 28  |            |             |
| 27  |            |             |
| 26  |            |             |
| 25  |            |             |
| 24  |            |             |
| 23  |            |             |
| 22  |            |             |
| 21  |            |             |
| 20  |            |             |
| 19  |            |             |
| 18  |            |             |
| 17  |            |             |
| 16  |            |             |
| 15  |            |             |
| 14  |            |             |
| 13  |            |             |
| 12  |            |             |
| 11  |            |             |
| 10  |            |             |
| 9   |            |             |
| 8   |            |             |
| 7   |            |             |
| 6   |            |             |
| 5   |            |             |
| 4   |            |             |
| 3   |            |             |
| 2   |            |             |
| 1   |            |             |
| 0   |            | Reset       |

CSI_BRIG_CSI_HOST_CM_EN Configures whether to enable CSI CM.
O: Disable. In this case, no data is output from CSI CM, and the downstream ISP cannot receive data.
1: Enable
(R/W)

CSI_BRIG_CSI_HOST_CM_BYPASS Configures whether to bypass CSI CM.
O: Do not bypass
1: Bypass
(R/W)

CSI_BRIG_CSI_HOST_CM_RX Configures the input image format of CSI CM.
0: RGB888
1: RGB565
2: YUV422
3: YUV420
(R/W)

CSI_BRIG_CSI_HOST_CM_RX_RGB_FORMAT Configures the channel order of input RGB data.
0: RGB
1: BGR
2: RGB
3: BRG
4: GRB
5: GBR
Others: Invalid
(R/W)

Continued on the next page...
```