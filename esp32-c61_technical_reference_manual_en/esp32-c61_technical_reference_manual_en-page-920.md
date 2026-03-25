

```markdown
Chapter 26  SPI Controller (SPI)

GoBack


1 If `GDMA_IN_SUC_EOF_CHn_INT` is triggered, it means all the RX data of GP-SPI2 has been stored in the RX buffer, and the TX data has been transferred to the slave.

2 `SPI_TRANS_DONE_INT` is triggered when CS is high, which indicates that master has completed the data exchange in `SPI_WO_REG~SPI_W15_REG` with slave in this mode.

3 If `SPI_DMA_SEG_TRANS_DONE_INT` is triggered, it means that the whole configurable segmented transfer (consisting of several segments) has finished, i.e., the RX data has been stored in the RX buffer completely and all the TX data has been sent out.
```