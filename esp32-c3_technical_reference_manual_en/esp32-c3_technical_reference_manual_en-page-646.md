

```markdown
| Transfer Type | Communication Mode | Controlled by | Interrupt |
|---------------|---------------------|---------------|-----------|
|||CPU|SPI_TRANS_DONE_INT|
|||DMA|SPI_DMA_SEG_TRANS_DONE_INT ³|
|Configurable Segmented Transfer|Full-duplex|CPU|Not supported|
||Half-duplex MOSI Mode|DMA|SPI_DMA_SEG_TRANS_DONE_INT|
|||CPU|Not supported|
||Half-duplex MISO|DMA|SPI_DMA_SEG_TRANS_DONE_INT|
|||CPU|Not supported|

Note:
1. If GDMA_IN_SUC_EOF_CHn_INT is triggered, it means all the RX data of GP-SPI2 has been stored in the RX buffer, and the TX data has been transferred to the slave.
2. SPI_TRANS_DONE_INT is triggered when CS is high, which indicates that master has completed the data exchange in SPI_WO_REG ~ SPI_W15_REG with slave in this mode.
3. If SPI_DMA_SEG_TRANS_DONE_INT is triggered, it means that the whole configurable segmented transfer (consisting of several segments) has finished, i.e. the RX data has been stored in the RX buffer completely and all the TX data has been sent out.

Table 27.9-2. GP-SPI2 Slave Mode Interrupts
| Transfer Type | Communication Mode | Controlled by | Interrupt |
|---------------|---------------------|---------------|-----------|
||Full-duplex|DMA|GDMA_IN_SUC_EOF_CHn_INT¹|
|||CPU|SPI_TRANS_DONE_INT²|
|Single Transfer|Half-duplex MOSI Mode|DMA (Wr_DMA)|GDMA_IN_SUC_EOF_CHn_INT³|
|||CPU (Wr_BUF)|SPI_TRANS_DONE_INT⁴|
|||DMA (Rd_DMA)|SPI_TRANS_DONE_INT⁵|
||Half-duplex MISO Mode|CPU (Rd_BUF)|SPI_TRANS_DONE_INT⁶|
|||DMA|GDMA_IN_SUC_EOF_CHn_INT⁷|
|||CPU|Not supported⁸|
|Slave Segmented Transfer|Half-duplex MOSI Mode|DMA (Wr_DMA)|SPI_DMA_SEG_TRANS_DONE_INT⁹|
|||CPU (Wr_BUF)|Not supported¹⁰|
||Half-duplex MISO Mode|DMA (Rd_DMA)|SPI_DMA_SEG_TRANS_DONE_INT¹¹|
|||CPU (Rd_BUF)|Not supported¹²|

Note:
1. If GDMA_IN_SUC_EOF_CHn_INT is triggered, it means all the RX data has been stored in the RX buffer, and the TX data has been sent to the slave.
2. SPI_TRANS_DONE_INT is triggered when CS is high, which indicates that master has completed the data exchange in SPI_WO_REG ~ SPI_W15_REG with slave in this mode.
3. SPI_SLV_WR_DMA_DONE_INT just means that the transmission on the SPI bus is done, but can not ensure that all the push data has been stored in the RX buffer. For this reason, GDMA_IN_SUC_EOF_CHn_INT is recommended.
4. Or wait for SPI_SLV_WR_BUF_DONE_INT.
```