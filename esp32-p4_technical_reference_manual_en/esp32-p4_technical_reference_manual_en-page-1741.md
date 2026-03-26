

```markdown
Register 36.145. CSI_BRIG_CSI_EN_REG (0x0004)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)        |                                                                             |
| ... |                    |                                                                             |
| 0   | Reset              | 0                                                                             |

CSI_BRIG_CSI_BRIG_EN Configures whether to enable CSI_Bridge.
O: Disable
1: Enable
(R/W)

Register 36.146. CSI_BRIG_BUF_FLOW_CTL_REG (0x000C)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| ... |                                      |                                                                             |
| 29  | CSIBRIG_CSI_BUF_DEPTH               | Represents the size of the CSI_Bridge buffer in use. (RO)                    |
| 16  | (reserved)                          |                                                                             |
| 15  | (reserved)                          |                                                                             |
| 13  |                                      |                                                                             |
| ... |                                      |                                                                             |
| 0   | Reset                                | 2040                                                                          |

CSI_BRIG_CSI_BUF_AFULL_THRD Configures the size threshold at which the CSI_Bridge buffer is about to be full. (R/W)

CSI_BRIG_CSI_BUF_DEPTH Represents the size of the CSI_Bridge buffer in use. (RO)
```