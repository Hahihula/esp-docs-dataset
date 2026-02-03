**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Heading:**
Interrupts Used in Master and Slave Modes

**Body Text with Table Descriptions:**

1. **Table Description:** 
   - "Table 30.10-1, GP-SPI Master Mode Interrupts"
   
2. **Content Summary for the First Table:**
   - The table lists different types of transfer (Single Transfer and Configurable Segmented Transfer) in various communication modes such as Full-duplex or Half-duplex MOSI Mode.
   - It specifies which components control these interrupts, including DMA, CPU, etc., with specific interrupt names like GDMA_IN_SUC_EOF_CHn_INT.

3. **Additional Information:**
   - If certain interrupts are triggered (e.g., GDMA_IN_SUC_EOF_CHn_INT), it indicates that all RX data of GP-SPI has been stored in the RX buffer and TX data transferred to the slave.
   - The note clarifies conditions for specific interrupts like SPITransDoneInt being high, indicating a completed master-slave exchange.

4. **Second Table Description:**
   - "Table 30.10-2, GP-SPI Slave Mode Interrupts"
   
5. **Content Summary for the Second Table:**
   - This table lists different transfer types (Single Transfer and Slave Segmented Transfer) in various communication modes.
   - It specifies which components control these interrupts like DMA or CPU with specific interrupt names such as GDMA_IN_SUC_EOF_CHn_INT.

6. **Additional Information about Interrupts for the Second Table:**
   - If certain interrupts are triggered, it indicates that all RX data has been stored in the buffer and TX data sent out.
   - The note clarifies conditions like DMA (Wr_DMA) or CPU (Rd BUFFER).

**Footer Text:** 
Espressif Systems
1150 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)

**Note:**
- There are references to "Continued on the next page" indicating that additional information is provided elsewhere in this document.
- Some notes and conditions for specific interrupts have numbers like [1], [2], etc., which likely correspond to footnotes or detailed explanations not visible here.

This structured description captures all textual content from both tables, their headings, descriptions of interrupt types based on transfer modes, components controlling the interrupts (DMA vs. CPU), as well as additional notes and conditions for specific interrupts in a clear markdown format suitable for further processing if needed.