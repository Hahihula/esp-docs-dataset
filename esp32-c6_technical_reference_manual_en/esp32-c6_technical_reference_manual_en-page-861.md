

```markdown
| Transfer Type                     | Communication Mode   | Controlled by     | Interrupt                                                                 |
|-----------------------------------|----------------------|-------------------|---------------------------------------------------------------------------|
| Single Transfer                  | Full-duplex          | DMA               | GDMA_IN_SUC_EOF_CHn_INT¹                                                |
|                                   |                      | CPU               | SPI_TRANS_DONE_INT²                                                      |
|                                   | Half-duplex MOSI     | DMA               | SPI_TRANS_DONE_INT                                                       |
|                                   |                      | CPU               | SPI_TRANS_DONE_INT                                                       |
|                                   | Half-duplex MISO     | DMA               | GDMA_IN_SUC_EOF_CHn_INT                                                  |
|                                   |                      | CPU               | SPI_TRANS_DONE_INT                                                       |
|                                   |                      |                   | SPI_DMA_SEG_TRANS_DONE_INT³                                             |

¹ If `GDMA_IN_SUC_EOF_CHn_INT` is triggered, it means all the RX data of GP-SPI2 has been stored in the RX buffer, and the TX data has been transferred to the slave.
² `SPI_TRANS_DONE_INT` is triggered when CS is high, which indicates that master has completed the data exchange in `SPI_WO_REG ~ SPI_W15_REG` with slave in this mode.
³ If `SPI_DMA_SEG_TRANS_DONE_INT` is triggered, it means that the whole configurable segmented transfer (consisting of several segments) has finished, i.e., the RX data has been stored in the RX buffer completely and all the TX data has been sent out.

Table 28.9-2. GP-SPI2 Interrupts as Slave
| Transfer Type                     | Communication Mode   | Controlled by     | Interrupt                                                                 |
|-----------------------------------|----------------------|-------------------|---------------------------------------------------------------------------|
| Single Transfer                  | Full-duplex          | DMA               | GDMA_IN_SUC_EOF_CHn_INT¹                                                |
|                                   |                      | CPU               | SPI_TRANS_DONE_INT²                                                      |
|                                   | Half-duplex MOSI     | DMA (Wr_DMA)      | GDMA_IN_SUC_EOF_CHn_INT³                                                 |
|                                   |                      | CPU (Wr_BUF)      | SPI_TRANS_DONE_INT⁴                                                      |
|                                   |                      | DMA (Rd_DMA)      | SPI_TRANS_DONE_INT⁵                                                      |
|                                   | Half-duplex MISO     | CPU (Rd_BUF)      | SPI_TRANS_DONE_INT⁶                                                      |
| Slave Segmented Transfer         | Full-duplex          | DMA               | GDMA_IN_SUC_EOF_CHn_INT⁷                                                 |
|                                   |                      | CPU               | Not supported⁸                                                            |
|                                   | Half-duplex MOSI     | DMA (Wr_DMA)      | SPI_DMA_SEG_TRANS_DONE_INT⁹                                             |
|                                   |                      | CPU (Wr_BUF)      | Not supported¹⁰                                                           |
|                                   | Half-duplex MISO     | DMA (Rd_DMA)      | SPI_DMA_SEG_TRANS_DONE_INT¹¹                                            |
|                                   |                      | CPU (Rd_BUF)      | Not supported¹²                                                           |

Continued on the next page
```