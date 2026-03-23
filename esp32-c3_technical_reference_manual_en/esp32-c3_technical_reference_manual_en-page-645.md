
```markdown
- SPI_SLV_EN_QPI_INT: triggered when En_QPI is received correctly in GP-SPI2 slave mode and the SPI transfer ends.
- SPI_SLV_CMD7_INT: triggered when CMD7 is received correctly in GP-SPI2 slave mode and the SPI transfer ends.
- SPI_SLV_CMD8_INT: triggered when CMD8 is received correctly in GP-SPI2 slave mode and the SPI transfer ends.
- SPI_SLV_CMD9_INT: triggered when CMD9 is received correctly in GP-SPI2 slave mode and the SPI transfer ends.
- SPI_SLV_CMDA_INT: triggered when CMDA is received correctly in GP-SPI2 slave mode and the SPI transfer ends.
- SPI_SLV_RD_DMA_DONE_INT: triggered at the end of Rd_DMA transfer in slave mode.
- SPI_SLV_WR_DMA_DONE_INT: triggered at the end of Wr_DMA transfer in slave mode.
- SPI_SLV_RD_BUF_DONE_INT: triggered at the end of Rd_BUF transfer in slave mode.
- SPI_SLV_WR_BUF_DONE_INT: triggered at the end of Wr_BUF transfer in slave mode.
- SPI_TRANS_DONE_INT: triggered at the end of SPI bus transfer in both master and slave modes.
- SPI_DMA_SEG_TRANS_DONE_INT: triggered at the end of End_SEG_TRANS transfer in GP-SPI2 slave segmented transfer mode or at the end of configurable segmented transfer in master mode.
- SPI_SEG_MAGIC_ERR_INT: triggered when a Magic error occurs in CONF buffer during configurable segmented transfer in master mode.
- SPI_MST_RX_AFIFO_WFUL_ERR_INT: triggered by RX AFIFO write-full error in GP-SPI2 master mode.
- SPI_MST_TX_AFIFO_REMPTY_ERR_INT: triggered by TX AFIFO read-empty error in GP-SPI2 master mode.
- SPI_SLV_CMD_ERR_INT: triggered when a received command value is not supported in GP-SPI2 slave mode.
- SPI_APP2_INT: used and triggered by software. It is only used for user defined function.
- SPI_APP1_INT: used and triggered by software. It is only used for user defined function.

Interrupts Used in Master and Slave Modes

Table 27.9-1 and Table 27.9-2 show the interrupts used in GP-SPI2 master and slave modes. Set the interrupt enable bit SPI_*_INT_ENA in SPI_DMA_INT_ENA_REG and wait for the SPI_INT interrupt. When the transfer ends, the related interrupt is triggered and should be cleared by software before the next transfer.

Table 27.9-1. GP-SPI2 Master Mode Interrupts

| Transfer Type     | Communication Mode   | Controlled by | Interrupt                                      |
|-------------------|----------------------|---------------|------------------------------------------------|
|                   |                      |               |                                                |
| Single Transfer   | Full-duplex          | DMA           | GDMA_IN_SUC_EOF_CHn_INT¹                       |
|                   |                      | CPU           | SPI_TRANS_DONE_INT²                            |
|                   | Half-duplex MOSI Mode| DMA           | SPI_TRANS_DONE_INT                             |
|                   |                      | CPU           | SPI_TRANS_DONE_INT                             |
|                   | Half-duplex MISO Mode| DMA           | GDMA_IN_SUC_EOF_TRM_INT                        |
```