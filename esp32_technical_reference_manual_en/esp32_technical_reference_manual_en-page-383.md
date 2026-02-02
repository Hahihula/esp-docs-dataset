**Title: Chapter 20 SPI Controller (SPI)**

**Subtitle: Register 20.30. SPI_DMA_INT_RAW_REG (0x114)**

**Diagram Description:** 
- A binary register diagram with labels for each bit position from least significant to most significant.
- Labels include:
  - `SPI_OUT_TOTAL_EOF_INT_RAW`
  - `SPI_INLink_DSCR_ERROR_INT_RAW`
  - `SPI_OUTLink_DSCR_ERROR_INT_RAW`
  - And others up to the last label at index '0'.

**Body Text:**
1. **SPI_OUT_TOTAL_EOF_INT_RAW**: The raw interrupt status bit for the SPI_OUT_TOTAL_EOF_INT interrupt.
2. **SPI_OUT_EOF_INT_RAW**: The raw interrupt status bit for the SPI_OUT_EOF_INT interrupt (RO).
3. **SPI_OUT_DONE_INT_RAW**: The raw interrupt status bit for the SPI_OUT_DONE_INT interrupt (RO).
4. **SPI_IN_SUC_EOF_INT_RAW**: The raw interrupt status bit for the SPI_IN_SUC_EOF_INT interrupt.
5. **SPI_IN_ERR_EOF_INT_RAW**: The raw interrupt status bit for the SPI_IN_ERR_EOF_INT interrupt.

6. **SPI_INlink_DSCR_ERROR_INT_RAW**: The raw interrupt status bit (RO).
7. **SPI_OUTlink_DSCR_ERROR_INT_RAW**: The raw interrupt status bit (RO).

8. **SPI_INLink_DSCR_EMPTY_INT_RAW**: The raw interrupt status bit for the SPI_INLink_DSCR_EMPTY_INT interrupt.

**Footer:**
- "Espressif Systems"
- Page number 383
- Document version ESP32 TRM (Version 5.6)
- Link to submit documentation feedback