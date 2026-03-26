

```markdown
## Register 36.156. CSI_BRIG_INT_ENA_REG (0x0028)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | CSI_BRIG_VADR_NUM_GT_INT_ENA               | Write 1 to enable CSI_BRIG_VADR_NUM_GT_INT. (R/W)                           |
| 29  | CSI_BRIG_VADR_NUM_LT_INT_ENA               | Write 1 to enable CSI_BRIG_VADR_NUM_LT_INT. (R/W)                           |
| 28  | CSI_BRIG_DISCARD_INT_ENA                   | Write 1 to enable CSI_BRIG_DISCARD_INT. (R/W)                               |
| 27  | CSI_BRIG_CSI_BUF_OVERRUN_INT_ENA           | Write 1 to enable CSI_BRIG_CSI_BUF_OVERRUN_INT. (R/W)                       |
| 26  | CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT_ENA        | Write 1 to enable CSI_BRIG_CSI_ASYNC_FIFO_OVF_INT. (R/W)                    |
| 25  | CSI_BRIG_DMA_CFG_HAS_UPDATED_INT_ENA       | Write 1 to enable CSI_BRIG_DMA_CFG_HAS_UPDATED_INT. (R/W)                   |

## Register 36.157. CSI_BRIG_HOST_CTRL_REG (0x0040)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 1   | 0                                           | Reset                                                                       |
| 0   | 1                                           | Reset                                                                       |

CSI_BRIG_CSI_ENABLECLK Configures whether to enable the clock lane of CSI PHY.
O: Disable
1: Enable
(R/W)
```