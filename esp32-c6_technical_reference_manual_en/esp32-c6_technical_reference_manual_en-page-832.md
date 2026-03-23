

```markdown
## 28.5.6.1 GDMA Configuration

- Select a GDMA channel, and configure a GDMA TX/RX descriptor. See Chapter 4 GDMA Controller (GDMA).
- Set the bit `GDMA_INLINK_START_CHn` or `GDMA_OUTLINK_START_CHn` to start GDMA RX engine and TX engine, respectively.
- Before all the GDMA TX buffer is used or the GDMA TX engine is reset, if `GDMA_OUTLINK_RESTART_CHn` is set, a new TX buffer will be added to the end of the last TX buffer in use.
- GDMA RX buffer is linked in the same way as the GDMA TX buffer, by setting `GDMA_INLINK_START_CHn` or `GDMA_INLINK_RESTART_CHn`.
- The TX and RX data lengths are determined by the configured GDMA TX and RX buffer respectively, both of which are 0 ~ 32 KB.
- Initialize GDMA inlink and outlink before GDMA starts. The bits `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` in register `SPI_DMA_CONF_REG` should be set, otherwise the read/write data will be stored to/sent from the registers `SPI_WO_REG ~ SPI_W15_REG`.

When operating as master, if `GDMA_IN_SUC_EOF_CHn_INT_ENA` is set, then the interrupt `GDMA_IN_SUC_EOF_CHn_INT` will be triggered when one single transfer or one configurable segmented transfer is finished.

When operating as slave, if `GDMA_IN_SUC_EOF_CHn_INT_ENA` is set, then the interrupt `GDMA_IN_SUC_EOF_CHn_INT` will be triggered when one of the following conditions are met.

Table 28.5-6. Interrupt Trigger Condition on GP-SPI2 Data Transfer as Slave

| Transfer Type             | Control Bit¹ | Control Bit² | Condition                                                                 |
|---------------------------|--------------|--------------|---------------------------------------------------------------------------|
| Slave Single Transfer     |              |              | A single transfer is done.                                                |
|                           | 0            | 0            | A single transfer is done. Or the length of the received data is equal to `(SPI_MS_DATA_BITLEN + 1)` |
|                           | 1            |              |                                                                           |
| Slave Segmented Transfer  |              |              | (CMD7 or End_SEG_TRANS) is received correctly.                            |
|                           | 0            | 1            | (CMD7 or End_SEG_TRANS) is received correctly. Or the length of the received data is equal to `(SPI_MS_DATA_BITLEN + 1)` |

¹ `SPI_RX_EOF_EN`
² `SPI_DMA_SLV_SEG_TRANS_EN`

## 28.5.6.2 GDMA TX/RX Buffer Length Control

It is recommended that the length of configured GDMA TX/RX buffer is equal to the length of actual data transferred.

- If the length of configured GDMA TX buffer is shorter than that of actual data transferred, the extra data will be the same as the last transferred data. `SPI_OUTFIFO_EMPTY_ERR_INT` and `GDMA_OUT_EOF_CHn_INT` are triggered.
- If the length of configured GDMA TX buffer is longer than that of actual data transferred, the TX buffer is not fully used, and the remaining buffer will be used for following transaction even if a new TX buffer is linked later. Please keep it in mind. Or save the unused data and reset DMA.
```