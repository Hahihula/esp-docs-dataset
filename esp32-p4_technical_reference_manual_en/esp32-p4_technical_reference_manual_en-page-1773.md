

```markdown
## Register 37.4. PPA_SRM_COLOR_MODE_REG (0x0020)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 14  |                             | Reset                                                                       |
| 13  |                             | Reset                                                                       |
| 12  |                             | Reset                                                                       |
| 11  |                             | Reset                                                                       |
| 10  |                             | Reset                                                                       |
| 9   |                             | Reset                                                                       |
| 8   |                             | Reset                                                                       |
| 7   |                             | Reset                                                                       |
| 6   |                             | Reset                                                                       |
| 5   |                             | Reset                                                                       |
| 4   |                             | Reset                                                                       |
| 3   |                             | Reset                                                                       |
| 2   |                             | Reset                                                                       |
| 1   |                             | Reset                                                                       |
| 0   |                             | Reset                                                                       |

### PPA_SRM_RX_CM
Configures the input image color format for SRM.
- O: ARGB8888
- 1: RGB888
- 2: RGB565
- 8: YUV420
Others: Reserved
(R/W)

### PPA_SRM_TX_CM
Configures the output image color format for SRM.
- O: ARGB8888
- 1: RGB888
- 2: RGB565
- 8: YUV420
Others: Reserved
(R/W)

### PPA_YUV_RX_RANGE
Configures the YUV range when the SRM input format is YUV.
- O: limit range
- 1: full range
(R/W)

### PPA_YUV_TX_RANGE
Configures the YUV range when the SRM output format is YUV.
- O: limit range
- 1: full range
(R/W)

### PPA_YUV2RGB_PROTOCOL
Configures the protocol used for the SRM input direction YUV to RGB.
- O: BT601
- 1: BT709
(R/W)

### PPA_RGB2YUV_PROTOCOL
Configures the protocol used for the SRM output direction RGB to YUV.
- O: BT601
- 1: BT709
(R/W)
```
Continued on the next page...
```