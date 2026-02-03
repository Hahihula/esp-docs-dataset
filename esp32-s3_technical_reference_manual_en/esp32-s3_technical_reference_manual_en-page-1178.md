**Title:**
Chapter 30 SPI Controller (SPI)

**Subtitle:**
Register 30.21. SPI_DMA_INT_ST_REG (0x0040)

**Menu/Navigation Link:**
GoBack

**Diagram Description with Labels and Values for Each Bit:**
- The diagram shows a register layout labeled as "SPI_DMA_INT_ST_REG" starting from bit position `31` to `0`.
- Bits are numbered sequentially, each associated with specific interrupt status bits.

**Interrupt Status Bits Descriptions (with corresponding registers):**

- **Bit 31:** SPI_DMA_INIFO_FULL_ERR_INT
  - Description: The status bit for SPI_DMA_INIFO_FULL_ERR_INT interrupt. (RO)
  
- **Bit 20 to Bit 4:** Reserved

- **Bit 19:** SPI_APPL_INT_ST
  - Description: The status bit for SPI_APPL_INT_ST interrupt.

- **Bit 18:** SPI_APP_INT_ST
  - Description: The status bit for SPI_APP_INT_ST interrupt.
  
- **Bit 17 to Bit 0:** Reserved

**Additional Interrupt Status Bits Descriptions (with corresponding registers):**

- **SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST**
  - Description: The status bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (RO)
  
- **SPI_SLV_EX_QPI_INT_ST**
  - Description: The status bit for SPI_SLV_EX_QPI_INT interrupt. (RO)

- **SPI_SLV_EN_QPI_INT_ST**
  - Description: The status bit for SPI_SLV_EN_QPI_INT interrupt.

- **SPI_SLV_CMD7_INT_ST**
  - Description: The status bit for SPI_SLV_CMD7_INT interrupt.
  
- **SPI_SLV_CMD8_INT_ST**
  - Description: The status bit for SPI_SLV_CMD8_INT interrupt. (RO)
  
- **SPI_SLV_CMD9_INT_ST**
  - Description: The status bit for SPI_SLV_CMD9_INT interrupt.

- **SPI_SLV_CMDMA_INT_ST**
  - Description: The status bit for SPI_SLV_CMDMA_INT interrupt.
  
- **SPI_SLV_RD_DMA_DONE_INT_ST**
  - Description: The status bit for SPI_SLV_RD_DMA_DONE_INT interrupt. (RO)
  
- **SPI_SLV_WR_DMA_DONE_INT_ST**
  - Description: The status bit for SPI_SLV_WR_DMA_DONE_INT interrupt.

- **SPI_SLV_RD_BUF_DONE_INT_ST**
  - Description: The status bit for SPI_SLV_RD_BUF_DONE_INT interrupt.
  
- **SPI_SLV_WR_BUF_DONE_INT_ST**
  - Description: The status bit for SPI_SLV_WR_BUF DONE_INT interrupt. (RO)
  
- **SPI_TRANS_DONE_INT_ST**
  - Description: The status bit for SPI TRANS DONE INT interrupt.

- **SPI_DMA_SEGTrans_DONE_INT_ST**
  - Description: The status bit for SPI_DMA_SEGTrans DONE INT interrupt.
  
- **SPI_SEG_MAGIC_ERR_INT_ST (for SPI2 only)**
  - Description: The status bit for SPI SEG MAGIC ERR INT interrupt. (RO)
  
- **SPI_SLV_CMD_ERR_INT_ST**
  - Description: The status bit for SPI SLV CMD ERR INT interrupt.

- **SPI_MST_RX_AFIFO_WFULL_ERR_INT_ST**
  - Description: The status bit for SPI MST RX AFIFO WFULL ERR INT interrupt.
  
**Footer Note:** Continued on the next page...

**Document Footer Information:**

- Company Name: Espressif Systems
- Document Version and Type:
  - ESP32-S3 TRM (Version 1.7)
- Page Numbering:
  - Current page number is not explicitly mentioned, but it's indicated to continue from a previous section.
- Submission Link/Feedback Option:
  - Submit Documentation Feedback

**Page Number:**
1178