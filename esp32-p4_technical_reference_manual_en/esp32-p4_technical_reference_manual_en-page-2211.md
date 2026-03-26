

```markdown
- Set `AXI_DMA_INLINK_START_CHn` or `AXI_DMA_OUTLINK_START_CHn` to start DMA RX or TX engine, respectively.
- Before all the DMA TX buffer is used or the DMA TX engine is reset, if `AXI_DMA_OUTLINK_RESTART_CHn` is set, a new TX buffer will be added to the end of the last TX buffer in use.
- DMA RX buffer is linked in the same way as the DMA TX buffer, by setting `AXI_DMA_INLINK_START_CHn` or `AXI_DMA_INLINK_RESTART_CHn`.
- The TX and RX data lengths are determined by the configured DMA TX and RX buffer respectively, both of which are 0~32 KB.
- Initialize DMA inlink and outlink before DMA starts. The bits `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` in register `SPI_DMA_CONF_REG` should be set, otherwise the read/write data will be stored to/sent from the registers `SPI_WO_REG~SPI_W15_REG`.

When GP-SPI operating as master, if `AXI_DMA_IN_SUC_EOF_CHn_INT_ENA` is set, then the interrupt `AXI_DMA_IN_SUC_EOF_CHn_INT` will be triggered when one single transfer or one configurable segmented transfer is finished.

When GP-SPI operating as slave, if `AXI_DMA_IN_SUC_EOF_CHn_INT_ENA` is set, then the interrupt `AXI_DMA_IN_SUC_EOF_CHn_INT` will be triggered when one of the following conditions are met.

Table 43.5-9. Interrupt Trigger Condition on GP-SPI Data Transfer as Slave

| Transfer Type           | Control Bit¹ | Control Bit² | Condition                                                                 |
|-------------------------|--------------|--------------|---------------------------------------------------------------------------|
| Slave Single Transfer   |              |              |                                                                           |
|                         | 0            | 0            | A single transfer is done.                                               |
|                         | 1            | 0            | A single transfer is done. Or the length of the received data is equal to `(SPI_MS_DATA_BITLEN + 1)`. |
| Slave Segmented Transfer|              |              |                                                                           |
|                         | 0            | 1            | CMD7 or `End_SEG_TRANS` is received correctly.                           |
|                         | 1            | 1            | CMD7 or `End_SEG_TRANS` is received correctly. Or the length of the received data is equal to `(SPI_MS_DATA_BITLEN + 1)`. |

¹ `SPI_RX_EOF_EN`
² `SPI_DMA_SLV_SEG_TRANS_EN`

43.5.7.2 DMA TX/RX Buffer Length Control

It is recommended that the length of the configured DMA TX/RX buffer is equal to the length of actual data transferred.

- If the length of the configured DMA TX buffer is shorter than that of the actual data transferred, the extra data will be the same as the last transferred data. `SPI_OUTFIFO_EMPTY_ERR_INT` and `AXI_DMA_OUT_EOF_CHn_INT` are triggered.
- If the length of the configured DMA TX buffer is longer than that of actual data transferred, the TX buffer is not fully used, and the remaining buffer will be used for the following transaction even if a new TX buffer is linked later. Please keep it in mind. Or save the unused data and reset the DMA.
- If the length of the configured DMA RX buffer is shorter than that of the actual data transferred, the extra data will be lost. `SPI_INFIFO_FULL_ERR_INT` and `SPI_TRANS_DONE_INT` are triggered. But `AXI_DMA_IN_SUC_EOF_CHn_INT` is not triggered.
```