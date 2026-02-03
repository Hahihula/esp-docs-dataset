**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Number and Title:**
30.10 Interrupts

**Subsection Heading:**
Interrupt Summary

**Body Text:**

GP-SPI provides SPI_INTR_2/3 interrupt interfaces. When an SPI transfer ends, an interrupt is generated in GP-SPI:

- **SPI_DMA_INFIFO_FULL_ERR_INT:** triggered when GDMA RX FIFO length is shorter than the real transferred data length.
  
- **SPI_DMA_OUTFIFO_EMPTY_ERR_INT:** triggered when GDMA TX FIFO length is shorter than the real transferred data length.

- **SPI_SLV_EX_QPI_INT:** triggered when Ex_QPI is received correctly in GP-SPI slave mode and the SPI transfer ends.

- **SPI_SLV_EN_QPI_INT:** triggered when En_QPI is received correctly in GP-SPI slave mode and the SPI transfer ends.

- **SPI_SLV_CMD7_INT:** triggered when CMD7 is received correctly in GP-SPI slave mode and the SPI transfer ends.

- **SPI_SLV_CMD8_INT:** triggered when CMD8 is received correctly in GP-SPI slave mode and the SPI transfer ends.

- **SPI_SLV_CMD9_INT:** triggered when CMD9 is received correctly in GP-SPI slave mode and the SPI transfer ends.

- **SPI_SLV_CMDA_INT:** triggered when CMDA is received correctly in GP-SPI slave mode and the SPI transfer ends.

- **SPI_SLV_RD_DMA_DONE_INT:** triggered at the end of Rd_DMA transfer in slave mode.
  
- **SPI_SLV_WR_DMA_DONE_INT:** triggered at the end of Wr_DMA transfer in slave mode.
  
- **SPI_SLV_RD_BUF_DONE_INT:** triggered at the end of RdBuf transfer in slave mode.

- **SPI_SLV_WR_BUF_DONE_INT:** triggered at the end of WrBuf transfer in slave mode.

- **SPITrans_DONE_INT:** triggered at the end of SPI bus transfer in both master and slave modes.
  
- **SPI_DMA_SEG TRANS DONE_INT:** triggered at the end of End_SegTrans in GP-SPI slave segmented transfer mode or at the end of configurable segmented transfer in master mode.

- **SPI_SEG MAGIC_ERR_INT:** triggered when a Magic error occurs in CONF buffer during configurable segmented transfer in master mode. (Only valid in GP-SPI2)

- **SPI_MST_RX_AFIFO_WFULL_ERR_INT:** triggered by RX AFIFO write-full error in GP-SPI master mode.
  
- **SPI_MST_TX_AFIFO_REMPPTY_ERR_INT:** triggered by TX AFIFO read-empty error in GP-SPI master mode.

- **SPI_SLV_CMD_ERR_INT:** triggered when a received command value is not supported in GP-SPI slave mode.

- **SPI_APP2_INT:** Set SPIAPP2_INT_SET to trigger this interrupt. It is only used for user defined function.
  
- **SPI_APP1_INT:** Set SPIAPP1_INT_SET to trigger this interrupt. It is only used for user defined function.

**Footer:**
Espressif Systems
Page number 1149, ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback