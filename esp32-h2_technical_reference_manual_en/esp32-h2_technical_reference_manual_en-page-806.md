

```markdown
| Transfer Type | Communication Mode | Controlled by | Interrupt |
|---------------|---------------------|---------------|-----------|
| Single Transfer | Full-duplex | DMA | GDMA_IN_SUC_EOF_CHn_INT¹ |
|               |                     | CPU | SPI_TRANS_DONE_INT² |
|               | Half-duplex MOSI | DMA (Wr_DMA) | GDMA_IN_SUC_EOF_CHn_INT³ |
|               |                     | CPU (Wr_BUF) | SPI_TRANS_DONE_INT⁴ |
|               | Half-duplex MISO | DMA (Rd_DMA) | SPI_TRANS_DONE_INT⁵ |
|               |                     | CPU (Rd_BUF) | SPI_TRANS_DONE_INT⁶ |
| Slave Segmented Transfer | Full-duplex | DMA | GDMA_IN_SUC_EOF_CHn_INT⁷ |
|                         |             | CPU | Not supported⁸ |
|                         | Half-duplex MOSI | DMA (Wr_DMA) | SPI_DMA_SEG_TRANS_DONE_INT⁹ |
|                         |                     | CPU (Wr_BUF) | Not supported¹⁰ |
|                         | Half-duplex MISO | DMA (Rd_DMA) | SPI_DMA_SEG_TRANS_DONE_INT¹¹ |
|                         |                     | CPU (Rd_BUF) | Not supported¹² |
```