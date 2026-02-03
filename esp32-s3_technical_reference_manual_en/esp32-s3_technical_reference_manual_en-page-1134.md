**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Body Text:**

- If `SPI_BIT_MAP_WORD[31:28] == SPI_DMA_SEG MAGIC_VALUE`, this DMA-controlled transfer continues normally; the interrupt `SPI_DMA_SEGTrans_Done_INT` is triggered at the end of this DMA-controlled transfer.
  
- If `SPI_BIT_MAP_WORD[31:28] != SPI_DMA_SEG MAGIC_VALUE, GP-SPI2 state (spi_st) goes back to IDLE and the transfer ends immediately. The interrupt `SPI_DMA_SEGTrans_Done_INT` is still triggered, with `SPI_SEG_Magic_ERR_INT_RAW` bit set to 1.

**Subheading:**
CONF Buffer Configuration Example

**Table Descriptions & Content:**

- **Table 30.5-12 and Table 30.5-13**: Provide an example of how to configure a CONF buffer for a transaction (segment i) in which `SPI_ADDR_REG, SPI_CTRL_REG, SPI_CLOCK_REG, SPI_USER_REG, SPI_USER1_REG` need to be updated.

**Table:**
- **Title:** Table 30.5-12. An Example of CONF buffer in Segment
- **Columns:** BM Bit Value | Register Name Note 
- **Rows:**
  - `SPI_ADDR_REG`: The first word in this buffer.
  - `SPI_CTRL_REG`: Second word, stores the new value to `SPI_CTRL_REG`.
  - `SPI_CLOCK_REG`: Third word, stores the new value to `SPI CLOCK REG`.
  - `SPI_USER_REG`: Fourth word, stores the new value to `SPI_USER REG`.
  - `SPI_USER1_REG`: Fifth and sixth words.

**Table:**
- **Title:** Table 30.5-13. BM Bit Value v.s. Register to Be Updated in This Example
- **Columns:** BM Bit | Value | Register Name 
- **Rows:**
  - `SPI_ADDR_REG`: BM Bit = [7, 8], Values = [0, 9]
  - `SPI_CTRL_REG`: BM Bit = [12, 13], Values = [0, 0]

**Notes:**  
In a DMA-controlled configurable segmented transfer, please pay special attention to the following bits:
- `SPI_USR_CONF`: set `SPIUSR_CONF` before `SPI_USR` is set.
- `SPI_USR_CONF_NXT`: if segment i is not the final transaction of this whole DMA-controlled transfer, its value should be 1.

**Additional Notes:**
- `GP-SPI2 CS setup time and hold time are programmable independently in each segment; see Section 30.6 for detailed configuration. The CS high time in each segment is about:**  
\[ (SPI_CONF_BITLEN + 5) \times T_{APB_CLK} \]

**Footer:**
Espressif Systems
1134 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback