**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header:**
Register 20.32. SPI_DMA_INT_CLR_REG (0x11C)

**Body Text with List and Descriptions of Registers:**

- **SPI_OUT_TOTAL_EOF_INT_CLR:** Set this bit to clear the SPI_OUT_TOTAL_EOF_INT interrupt.
- **SPI_OUT_EOF_INT_CLR:** Set this bit to clear the SPI_OUT_EOF_INT interrupt. (R/W)
- **SPI_OUT_DONE_INT_CLR:** Set this bit to clear the SPI_OUTDone_INT interrupt. (R/W)
- **SPI_IN_SUC_EOF_INT_CLR:** Set this bit to clear the SPI_IN_SUC_EOF_INT interrupt.
- **SPI_IN_ERR_EOF_INT_CLR:** Set this bit to clear the SPI_IN_ERR_EOF_INT interrupt.
- **SPI_IN_DONE_INT_CLR:** Set this bit to clear the SPI_IN_DONE_INT interrupt. (R/W)
- **SPI_INLInk_DSCR_ERROR_INT_CLR:** Set this bit to clear the SPI_INLInk_DSCR_ERROR_INT interrupt.

**Additional Registers:**

- **SPI_OUTLINK_DSCR_ERROR_INT_CLR:** Set this bit to clear the SPI_OUTLINK_DSCR_ERROR_INT interrupt.
- **SPI_INLInk_DSCR_EMPTY_INT_CLR:** Set this bit to clear the SPI_INLInk_DSCR_EMPTY_INT interrupt. (R/W)

**Register 20.33:**
- **SPI_IN_ERR_EOFDES_ADDR_REG (0x120):** The inlink descriptor address when SPI DMA encountered an error in receiving data.

**Register 20.34:**
- **SPI_IN_SUC_EOFDES_ADDR_REG (0x124):** The last inlink descriptor address when SPI DMA encountered EOF.
- **SPI_IN_SUC_EOFDES_ADDR_REG:** The last inlink descriptor address when SPI DMA encountered EOF. (RO)

**Footer Information:**
Espressif Systems
385 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack