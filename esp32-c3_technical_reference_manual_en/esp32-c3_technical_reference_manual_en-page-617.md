

```markdown
- Data is received in DMA-controlled mode but sent in CPU-controlled mode.
- Data is received in CPU-controlled mode but sent in DMA-controlled mode.
- Data is received in CPU-controlled mode and sent in CPU-controlled mode.

## 27.5.6.1 GDMA Configuration

- Select a GDMA channel, and configure a GDMA TX/RX descriptor, see Chapter 2 GDMA Controller (GDMA).
- Set the bit `GDMA_INLINK_START_CHn` or `GDMA_OUTLINK_START_CHn` to start GDMA RX/TX engine.
- Before all the GDMA TX buffer is used or the GDMA TX engine is reset, if `GDMA_OUTLINK_RESTART_CHn` is set, a new TX buffer will be added to the end of the last TX buffer in use.
- GDMA RX buffer is linked in the same way as the GDMA TX buffer, by setting `GDMA_INLINK_START_CHn` or `GDMA_INLINK_RESTART_CHn`.
- The TX and RX data lengths are determined by the configured GDMA TX and RX buffer respectively, both of which are 0 ~ 32 KB.
- Initialize GDMA inlink and outlink before GDMA starts. The bits `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` in register `SPI_DMA_CONF_REG` should be set, otherwise the read/write data will be stored to/sent from the registers `SPI_WO_REG ~ SPI_W15_REG`.

In master mode, if `GDMA_IN_SUC_EOF_CHn_INT_ENA` is set, then the interrupt `GDMA_IN_SUC_EOF_CHn_INT` will be triggered when one single transfer or one configurable segmented transfer is finished.

The only difference between DMA-controlled transfers in master mode and in slave mode is on the GDMA RX control:

- When the bit `SPI_RX_EOF_EN` is cleared, a GDMA_IN_SUC_EOF_CHn_INT interrupt may be generated after the CS is pulled high once:
  - In a slave single transfer, if `SPI_DMA_SLV_SEG_TRANS_EN` is cleared and `GDMA_IN_SUC_EOF_CHn_INT` _ENA_ is set, a GDMA_IN_SUC_EOF_CHn_INT interrupt will be triggered once the single transfer is done.
  - In a slave segmented transfer, if both `SPI_DMA_SLV_SEG_TRANS_EN` and `GDMA_IN_SUC_EOF_CHn_INT_ENA` are set, a GDMA_IN_SUC_EOF_CHn_INT interrupt also is triggered once the command (CMD7 or End_SEG_TRANS) is received correctly.

- When the bit `SPI_RX_EOF_EN` is set, the generation of `GDMA_IN_SUC_EOF_CHn_INT` also depends on the length of transferred data.
  - In a slave single transfer, if `SPI_DMA_SLV_SEG_TRANS_EN` is cleared and `GDMA_IN_SUC_EOF_CHn_INT_ENA` is set, a GDMA_IN_SUC_EOF_CHn_INT interrupt will be generated once the single transfer is done or the length of GDMA RX received data is equal to `(SPI_MS_DATA_BITLEN + 1)`.
  - In a slave segmented transfer, if `SPI_DMA_SLV_SEG_TRANS_EN` is set, a GDMA_IN_SUC_EOF_CHn_INT interrupt will be generated once the command (CMD7 or
```