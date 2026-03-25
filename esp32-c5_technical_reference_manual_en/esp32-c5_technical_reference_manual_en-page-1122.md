

```markdown
## 33.5.7 DMA-Controlled Data Transfer

DMA-controlled transfer refers to the transfer in which the GDMA RX module receives data and the GDMA TX module sends data. This transfer is supported when the GP-SPI2 works as master or as slave.

A DMA-controlled transfer can be:

*   a single transfer, consisting of only one transaction. GP-SPI2 supports this transfer when it works as master or as slave.
*   a configurable segmented transfer, consisting of several transactions (segments). GP-SPI2 supports this transfer only when works as a master. For more information, see Section 33.5.9.5.
*   a slave segmented transfer, consisting of several transactions (segments). GP-SPI2 supports this transfer only when works as a slave. For more information, see Section 33.5.10.3.

A DMA-controlled transfer only needs to be triggered once by CPU. When such a transfer is triggered, data is transferred by the DMA engine from or to the DMA-linked memory, without CPU operation.

DMA-controlled transfer supports full-duplex communication, half-duplex communication, and functions described in Section 33.5.9 and Section 33.5.10. Meanwhile, the GDMA RX module is independent from the GDMA TX module, which means that there are four kinds of full-duplex communications:

*   Data is received in DMA-controlled mode and sent in DMA-controlled mode.
*   Data is received in DMA-controlled mode but sent in CPU-controlled mode.
*   Data is received in CPU-controlled mode but sent in DMA-controlled mode.
*   Data is received in CPU-controlled mode and sent in CPU-controlled mode.

### 33.5.7.1 DMA Configuration

*   Select a GDMA channel `n` and configure GDMA TX/RX descriptor. See Chapter 5 GDMA Controller (GDMA).
*   Set `AHB_DMA_INLINK_START_CHn` or `AHB_DMA_OUTLINK_START_CHn` to start DMA RX or TX engine, respectively.
*   Before all the GDMA TX buffer is used or the GDMA TX engine is reset, if `AHB_DMA_OUTLINK_RESTART_CHn` is set, a new TX buffer will be added to the end of the last TX buffer in use.
*   GDMA RX buffer is linked in the same way as the GDMA TX buffer, by setting `AHB_DMA_INLINK_START_CHn` or `AHB_DMA_INLINK_RESTART_CHn`.
*   The TX and RX data lengths are determined by the configured GDMA TX and RX buffer respectively, both of which are 0~32 KB.
*   Initialize GDMA inlink and outlink before GDMA starts. The bits `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` in register `SPI_DMA_CONF_REG` should be set, otherwise the read/write data will be stored to/sent from the registers `SPI_W0_REG~SPI_W15_REG`.

When GP-SPI2 operates as master, if `AHB_DMA_IN_SUC_EOF_CHn_INT_ENA` is set, then the interrupt `AHB_DMA_IN_SUC_EOF_CHn_INT` will be triggered when one single transfer or one configurable segmented transfer is finished.
```