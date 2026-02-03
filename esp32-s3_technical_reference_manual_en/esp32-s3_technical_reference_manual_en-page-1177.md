**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Navigation Link:**
GoBack

**Register Information:**
- **Register Name:** Register 30.20.
- **Register Address:** SPI_DMA_INT_RAW_REG (0x003C)
- **Continuation Note:** Continued from the previous page...

**Interrupt Descriptions and Raw Bits for Various Interrupts in SPI_DMA:**

1. **SPI_DMA_SEG_TRANS_DONE_INT_RAW**
   - Description: The raw bit for SPI_DMA_SEG_TRANSDone_INT interrupt.
   - Access Type: Read/Write (R/WTC/SS)

2. **SPI_SEG MAGIC_ERR_INT_RAW (for SPI2 only)**
   - Description: The raw bit for SPI_SEG_MAGIC_ERR_INT interrupt.
   - Access Type: Read/Write (R/WTC/SS)

3. **SPI_SLV_CMD_ERR_INT_RAW**
   - Description: The raw bit for SPI_SLV_CMD_ERR_int interrupt.
   - Access Type: Read/Write (R/WTC/SS)

4. **SPI_MST_RX_A FIFO_WFULL_ERR_INT_RAW**
   - Description: The raw bit for SPI_MST_RX_A FIFO_WfullErr_INT interrupt.
   - Access Type: Read/Write (R/WTC/SS)

5. **SPI_MST_TX_A FIFO_REMPTY_INT_RAW**
   - Description: The raw bit for SPI_MST_TX_A FIFO_Rempty_INT interrupt.
   - Access Type: Read/Write (R/WTC/SS)

6. **SPI_APP2_INT_RAW**
   - Description: The raw bit for SPI_APP2_INT interrupt. Note that the value is only controlled by software, with access type being Read/Write (R/WTC/SS).

7. **SPI_APP1_INT_RAW**
   - Description: The raw bit for SPI_APP1_INT interrupt. Similar to SPI_APP2, its value can be managed solely through software control.

**Footer Information:**
- Company Name:** Espressif Systems
- Document Version and Type:** ESP32-S3 TRM (Version 1.7)
- Page Number:** 1177

**Additional Links:**
- Submit Documentation Feedback