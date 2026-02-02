**Title:**
Chapter 20 SPI Controller (SPI)

**Menu/Navigation Link:**
GoBack

**Register Information:**
- **Register Name:** Register 20.29. SPI_DMA_INT_ENA_REG (0x110)
- **Binary Diagram Description:** Binary diagram showing the layout of bits in register, with labels for each bit from `SPI_OUT_TOTAL_EOF_INT_ENA` to `SPI_INLink_DSCR_EMPTY_INT_ENA`.

**Text Descriptions:**
1. **SPI_OUT_TOTAL_EOF_INT_ENA**: The interrupt enable bit for the SPI_OUT_TOTAL_EOF_INT_interrupt.
   - (R/W)
2. **SPI_OUT_EOF_INT_ENA**: The interrupt enable bit for the SPI_OUT_EOF_INT_interrupt.
   - (R/W)
3. **SPI_OUTDone_INT_ENA**: The interrupt enable bit for the SPI_OUT_DONE_INT_interrupt.
   - (R/W)
4. **SPI_IN_SUC_EOF_INT_ENA**: The interrupt enable bit for the SPI_IN_SUC_EOF_INT_interrupt.
   - (R/W)
5. **SPI_IN_ERR_EOF_INT_ENA**: The interrupt enable bit for the SPI_IN_ERR_EOF_INT_interrupt.
   - (R/W)
6. **SPI_IN_DONE_INT_ENA**: The interrupt enable bit for the SPI_IN_DONE_INT_interrupt.
   - (R/W)

**Interrupt Details:**
- **SPI_INLink_DSCR_ERROR_INT_ENA**: The interrupt enable bit for the SPI_INLink_DSCR_ERROR_INT_interrupt.
  - (R/W)
- **SPI_OUTlink_DSCR_ERROR_INT_ENA**: The interrupt enable bit for the SPI_OUTlink_DSCR_ERROR_INT_interrupt.
  - (R/W)

**Additional Information:**
- **SPI_INLink_DSCR_EMPTY_INT_ENA**: The interrupt enable bit for the SPI_INlink_DSCR_EMPTY_INT_interrupt.
  - (R/W) 

**Footer:**
- Page number and document version information:
  - "382 ESP32 TRM (Version 5.6)"
- Company name at bottom left corner:
  - Espressif Systems
- Link for submitting documentation feedback:
  - Submit Documentation Feedback