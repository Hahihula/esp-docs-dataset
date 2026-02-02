**Title:**
Chapter 20 SPI Controller (SPI)

**Header:**
Register 20.31. SPI_DMA_INT_ST_REG (0x118)

**Binary Representation Diagram:**
- The diagram shows a binary representation of the register with bits labeled from right to left as follows:
  - Reset
  - SPI_OUT_TOTAL_EOF_INT_ST
  - (reserved)
  - ...
  - SPI_INLINK_DSCR_ERROR_INT_ST

**Register Description Table:**

1. **SPI_OUT_TOTAL_EOF_INT_ST**
   - The masked interrupt status bit for the SPI_OUT_TOTAL_EOF_INT interrupt.
   - Read/Write (RO)

2. **SPI_OUT_EOF_INT_ST**
   - The masked interrupt status bit for the SPI_OUT_EOF_INT interrupt.
   - Read/Write (RO)

3. **SPI_OUT_DONE_INT_ST**
   - The masked interrupt status bit for the SPI_OUTDone_INT interrupt.
   - Read/Write (RO)

4. **SPI_IN_SUC_EOF_INT ST**
   - The masked interrupt status bit for the SPI_INSuc_EOF_INT interrupt.
   - Read/Write (RO)

5. **SPI_IN_ERR_EOF_INT_ST**
   - The masked interrupt status bit for the SPI_INErr_EOF_INT interrupt.
   - Read/Write (RO)

6. **SPI_IN_DONE_INT ST**
   - The masked interrupt status bit for the SPI_INDone_INT interrupt.
   - Read/Write (RO)

7. **SPI_INLINK_DSCR_ERROR_INT_ST**
   - The masked interrupt status bit for the SPI_INlink_DSCR_Error_INT interrupt.
   - Read/Write (RO)

8. **SPI_OUTLINK_DSCR_ERROR_INT ST**
   - The masked interrupt status bit for the SPI_Outlink_DSCR_Error_INT interrupt.
   - Read/Write (RO)

9. **SPI_INLINK_DSCR_EMPTY_INT_ST**
   - The masked interrupt status bit for the SPI_Inlink_DSCR_Empty_INT interrupt.
   - Read/Write (RO)

**Footer:**
Espressif Systems
384 ESP32 TRM (Version 5.6)
Submit Documentation Feedback