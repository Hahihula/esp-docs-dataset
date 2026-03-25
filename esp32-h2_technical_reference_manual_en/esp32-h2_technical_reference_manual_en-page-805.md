
```markdown
- SPI_DMA_SEG_TRANS_DONE_INT: triggered at the end of End_SEG_TRANS transfer in GP-SPI2 slave segmented transfer mode or at the end of configurable segmented transfer as master.
- SPI_SEG_MAGIC_ERR_INT: triggered when a Magic error occurs in CONF buffer during configurable segmented transfer as master.
- SPI_MST_RX_AFIFO_WFULL_ERR_INT: triggered by RX AFIFO write-full error in GP-SPI2 as master.
- SPI_MST_TX_AFIFO_REMPTY_ERR_INT: triggered by TX AFIFO read-empty error in GP-SPI2 as master.
- SPI_SLV_CMD_ERR_INT: triggered when a received command value is not supported in GP-SPI2 as slave.
- SPI_APP2_INT: used and triggered by software. Only used for user defined function.
- SPI_APP1_INT: used and triggered by software. Only used for user defined function.

Interrupts Used as Master and Slave

Table 29.9-1 and Table 29.9-2 show the interrupts used in GP-SPI2 as master and as slave, respectively. Set the interrupt enable bit SPI_*_INT_ENA in SPI_DMA_INT_ENA_REG and wait for the SPI_INTR interrupt. When the transfer ends, the related interrupt is triggered and should be cleared by software before the next transfer.

Table 29.9-1. GP-SPI2 Interrupts as Master

| Transfer Type             | Communication Mode | Controlled by | Interrupt                                                                 |
|----------------------------|---------------------|---------------|---------------------------------------------------------------------------|
| Single Transfer           |                     |               |                                                                           |
|                            | Full-duplex         | DMA           | GDMA_IN_SUC_EOF_CHn_INT¹                                                |
|                            |                    | CPU           | SPI_TRANS_DONE_INT²                                                      |
|                            | Half-duplex MOSI    | DMA           | SPI_TRANS_DONE_INT                                                       |
|                            |                    | CPU           | SPI_TRANS_DONE_INT                                                       |
|                            | Half-duplex MISO    | DMA           | GDMA_IN_SUC_EOF_CHn_INT¹                                                |
|                            |                    | CPU           | SPI_TRANS_DONE_INT                                                       |
|                            |                     |               | SPI_DMA_SEG_TRANS_DONE_INT³                                             |
| Configurable Segmented Transfer | Full-duplex         | DMA           | Not supported                                                             |
|                            |                    | CPU           | SPI_DMA_SEG_TRANS_DONE_INT                                               |
|                            | Half-duplex MOSI    | DMA           | Not supported                                                             |
|                            |                    | CPU           | SPI_DMA_SEG_TRANS_DONE_INT                                               |
|                            | Half-duplex MISO    | DMA           | Not supported                                                             |
|                            |                    | CPU           | Not supported                                                             |

¹ If GDMA_IN_SUC_EOF_CHn_INT is triggered, it means all the RX data of GP-SPI2 has been stored in the RX buffer, and the TX data has been transferred to the slave.
² SPI_TRANS_DONE_INT is triggered when CS is high, which indicates that master has completed the data exchange in SPI_WO_REG ~ SPI_W15_REG with slave in this mode.
³ If SPI_DMA_SEG_TRANS_DONE_INT is triggered, it means that the whole configurable segmented transfer (consisting of several segments) has finished, i.e., the RX data has been stored in the RX buffer completely and all the TX data has been sent out.
```