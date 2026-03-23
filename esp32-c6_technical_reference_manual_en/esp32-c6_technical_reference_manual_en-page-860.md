
```markdown
- SPI_SLV_EN_QPI_INT: triggered when En_QPI is received correctly in GP-SPI2 as slave and the SPI transfer ends.
- SPI_SLV_CMD7_INT: triggered when CMD7 is received correctly in GP-SPI2 as slave and the SPI transfer ends.
- SPI_SLV_CMD8_INT: triggered when CMD8 is received correctly in GP-SPI2 as slave and the SPI transfer ends.
- SPI_SLV_CMD9_INT: triggered when CMD9 is received correctly in GP-SPI2 as slave and the SPI transfer ends.
- SPI_SLV_CMDA_INT: triggered when CMDA is received correctly in GP-SPI2 as slave and the SPI transfer ends.
- SPI_SLV_RD_DMA_DONE_INT: triggered at the end of Rd_DMA transfer as slave.
- SPI_SLV_WR_DMA_DONE_INT: triggered at the end of Wr_DMA transfer as slave.
- SPI_SLV_RD_BUF_DONE_INT: triggered at the end of Rd_BUF transfer as slave.
- SPI_SLV_WR_BUF_DONE_INT: triggered at the end of Wr_BUF transfer as slave.
- SPI_TRANS_DONE_INT: triggered at the end of SPI bus transfer in both as master and as slave.
- SPI_DMA_SEG_TRANS_DONE_INT: triggered at the end of End_SEG_TRANS transfer in GP-SPI2 slave segmented transfer mode or at the end of configurable segmented transfer as master.
- SPI_SEG_MAGIC_ERR_INT: triggered when a Magic error occurs in CONF buffer during configurable segmented transfer as master.
- SPI_MST_RX_AFIFO_WFULL_ERR_INT: triggered by RX AFIFO write-full error in GP-SPI2 as master.
- SPI_MST_TX_AFIFO_REMPTY_ERR_INT: triggered by TX AFIFO read-empty error in GP-SPI2 as master.
- SPI_SLV_CMD_ERR_INT: triggered when a received command value is not supported in GP-SPI2 as slave.
- SPI_APP2_INT: used and triggered by software. Only used for user defined function.
- SPI_APP1_INT: used and triggered by software. Only used for user defined function.

Interrupts Used as Master and Slave

Table 28.9-1 and Table 28.9-2 show the interrupts used in GP-SPI2 as master and as slave, respectively. Set the interrupt enable bit SPI_*_INT_ENA in SPI_DMA_INT_ENA_REG and wait for the SPI_INT interrupt. When the transfer ends, the related interrupt is triggered and should be cleared by software before the next transfer.
```