**Title:**
Chapter 30 SPI Controller (SPI)

**Header:**
Register 30.20. SPI_DMA_INT_RAW_REG (0x003C)

**Diagram Description:**
A diagram showing the layout of a register with various fields labeled, such as "SPI Appl", "SPI APP1", etc., and some bits marked in red.

**Body Text:**

- **Field Descriptions:** 
  - SPI_DMA_INFIFO_FULL_ERR_INT_RAW
    - The raw bit for SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (R/WTC/SS)
  - SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW
    - The raw bit for SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt.
  - SPI_SLV_EX_QPI_INT_RAW
    - The raw bit for SPI_SLV_EX_QPI_INT interrupt.
  - SPI_SLV_EN_QPI_INT_RAW
    - The raw bit for SPI_SLV_EN_QPI_INT interrupt. (R/WTC/SS)
  - SPI_SLV_CMD7_INT_RAW
    - The raw bit for SPI_SLV_CMD7_INT interrupt. (R/WTC/SS)
  - SPI_SLV_CMD8_INT_RAW
    - The raw bit for SPI_SLV_CMD8_INT interrupt.
  - SPI_SLV_CMD9_INT_RAW
    - The raw bit for SPI_SLV_CMD9_INT interrupt. (R/WTC/SS)
  - SPI_SLV_CMDA_INT_RAW
    - The raw bit for SPI_SLV_CMDA_INT interrupt. (R/WTC/SS)
  - SPI_SLV_RD_DMA_DONE_INT_RAW
    - The raw bit for SPI_SLV_RD_DMA_DONE_INT interrupt.
  - SPI_SLV_WR_DMA_DONE_INT_RAW
    - The raw bit for SPI_SLV_WR_DMA_DONE_INT interrupt.

**Continuation Note:**
Continued on the next page...

**Footer Information:**
Espressif Systems  
1176  
ESP32-S3 TRM (Version 1.7)  

**Link:**
Submit Documentation Feedback