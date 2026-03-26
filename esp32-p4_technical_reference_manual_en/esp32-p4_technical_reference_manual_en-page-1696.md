

```markdown
Register 36.43. ISP_AE_MONITOR_REG (0x0004)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                 |                                                                             |
| 22  | ISP_AE_MONITOR_TH          | Configures the upper threshold for AE luminance monitoring. (R/W)            |
| 21  | ISP_AE_MONITOR_TL          | Configures the lower threshold for AE luminance monitoring. (R/W)            |
| 16  | ISP_AE_MONITOR_PERIOD      | Configures the frame interval for AE monitoring. (R/W)                       |
| 7   | Reset                      |                                                                             |

ISP_AE_MONITOR_TL    Configures the lower threshold for AE luminance monitoring. (R/W)
ISP_AE_MONITOR_TH    Configures the upper threshold for AE luminance monitoring. (R/W)
ISP_AE_MONITOR_PERIOD Configures the frame interval for AE monitoring. (R/W)

Register 36.44. ISP_AE_BX_REG (0x0008)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                 |                                                                             |
| 22  | ISP_AE_X_START             | Configures the start coordinate of the AE statistical window in the horizontal direction. (R/W) |
| 11  | ISP_AE_X_BSIZE             | Configures the horizontal size of each sub-window. (R/W)                     |

ISP_AE_X_BSIZE    Configures the horizontal size of each sub-window. (R/W)
ISP_AE_X_START    Configures the start coordinate of the AE statistical window in the horizontal direction. (R/W)

Register 36.45. ISP_AE_BY_REG (0x00CC)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                 |                                                                             |
| 22  | ISP_AE_Y_START             | Configures the start coordinate of the AE statistical window in the vertical direction. (R/W) |
| 11  | ISP_AE_Y_BSIZE             | Configures the vertical dimension of each sub-window. (R/W)                  |

ISP_AE_Y_BSIZE    Configures the vertical dimension of each sub-window. (R/W)
ISP_AE_Y_START    Configures the start coordinate of the AE statistical window in the vertical direction. (R/W)
```