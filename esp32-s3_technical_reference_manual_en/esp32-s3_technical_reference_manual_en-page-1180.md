**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.22. SPI_DMA_INT_SET_REG (0x0044)

**Body Text with Descriptions of Register Bits and Interrupts:**

Continued from the previous page...

- **SPI_SLV_RD_DMA_DONE_INT_SET**: The software set bit for SPI_SLV_RD_DMADone_INT interrupt.
- **SPI_SLV_WR_DMA_DONE_INT_SET**: The software set bit for SPI_SLV_WR_DMA_DONE_INT interrupt.
- **SPI_SLV_RDBUF_DONE_INT_SET**: The software set bit for SPI_SLV_RDBUF_DONE_INT interrupt.
- **SPI_SLV_WRBUF_DONE_INT_SET**: The software set bit for SPI_SLV_WRBUF_DONE_INT interrupt.
- **SPITransDoneIntSet**: The software set bit for SPI_TRANS_DONE_INT interrupt.

**Additional Interrupts:**
- **SPI_DMA_SEGTransDoneIntSet**: The software set bit for SPI_DMA_SEGTransDone_INT interrupt (for SPI2 only).
- **SPI_SegMagicErrIntSet**: The software set bit for SPI_SEG_MagicErr_INT interrupt.
- **SPI_SLV_CmdErrIntSet**: The software set bit for SPI_SLV_CmdErr_INT interrupt.

**Interrupts Related to FIFO and Error Handling:**
- **SPI_MST_RX_AFIFO_WFULLErrIntSet**: The software set bit for SPI_MST_RX_AFIFO_WFULLErr_INT interrupt.
- **SPI_MST_TX_AFIFO_RemptyErrIntSet**: The software set bit for SPI_MST_TX_AFIFO_REMPTYErr_INT interrupt.

**Additional Interrupts:**
- **SPI_APP2_INT_SET**: The software set bit for SPI_APP2_INT interrupt (for SPI1).
- **SPI_APP1_INT_SET**: The software set bit for SPI_APP1_INT interrupt.

**Register 30.23, SPI_WO_REG (0x0098):**

- **SPI_BUFO**: 32-bit data buffer O. (R/W/SS)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)