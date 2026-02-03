**Title: Chapter 30 SPI Controller (SPI)**

**Subtitle: Register 30.19. SPI_DMA_INT_CLR_REG (0x0038)**

**Diagram Description:** 
- A diagram showing the layout of a register with various fields labeled, such as "SPI_DMA_INIFO_FULL_ERR_INT_CLR," "SPI_APPL_INT_ERR_INT_CLR," and others.

**Table:**
| Field Name | Description |
|------------|-------------|
| SPI_DMA_INIFO_FULL_ERR_INT_CLR | The clear bit for SPI_DMA_INIFO_FULL_ERR_INT interrupt. (WT) |
| SPI_DMA_OUTFIFO_EMPTY_ERR_INT_CLR | The clear bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (WT) |
| SPI_EX_QPI_INT_CLR | The clear bit for SPI_EX_QPI_INT interrupt. (WT) |
| SPI_EN_QPI_INT_CLR | The clear bit for SPI_EN_QPI_INT interrupt. (WT) |
| SPI_CMD7_INT_CLR | The clear bit for SPI_CMD7_INT interrupt. (WT) |
| SPI_CMD8_INT_CLR | The clear bit for SPI_CMD8_INT interrupt. (WT) |
| SPI_CMD9_INT_CLR | The clear bit for SPI_CMD9_INT interrupt. (WT) |
| SPI_CMDA_INT_CLR | The clear bit for SPI_CMDA_INT interrupt. (WT) |
| SPI_RD_DMA_DONE_INT_CLR | The clear bit for SPI_RD_DMA_DONE_INT interrupt. (WT) |
| SPI_WR_DMADone_INT_CLR | The clear bit for SPI_WR_DMADone_INT interrupt. (WT) |
| SPI_RD_BUF_DONE_INT_CLR | The clear bit for SPI_RD_BUF_DONE_INT interrupt. (WT) |
| SPI_WRBuf_DONE_INT_CLR | The clear bit for SPI_WRBuf_DONE_INT interrupt. (WT) |
| SPITrans_DONE_INT_CLR | The clear bit for SPITrans_DONE_INT interrupt. (WT) |
| SPI_DMA_SEGTrans_DONE_INT_CLR | The clear bit for SPI_DMA_SEGTrans_DONE_INT interrupt. (WT) |
| SPI_Magic_ERR_INT_CLR (for SPI2 only) | The clear bit for SPI_Seg_Magic_ERR_INT interrupt. (WT) |
| SPI_CMD_ERR_INT_CLR | The clear bit for SPI_Cmd_ERR_INT interrupt. (WT) |

**Footer:**
- "Espressif Systems"
- Page number 1174
- Document version ESP32-S3 TRM (Version 1.7)
- Link to submit documentation feedback