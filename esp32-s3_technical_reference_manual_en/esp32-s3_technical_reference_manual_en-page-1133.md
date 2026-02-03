**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Body Text with Steps and Instructions:**

9. Configure all the needed CONF buffers, TX buffers and RX buffers, respectively for each segment before this DMA-controlled transfer begins.

10. Point `GDMA_OUTLINK_ADDR_CHn` to the head address of the CONF and TX buffer descriptor linked list, and then set `GDMA_OUTLINK_START_CHn` to start the TX GDMA.

11. Clear the bit `SPI_RX_EOF_EN` in register `SPI_DMA_CONF_REG`. Point `GDMA_INLINK_ADDR_CHn` to the head address of the RX buffer descriptor linked list, and then set `GDMA_INLINK_START_CHn` to start the RX GDMA.

12. Set `SPI_USR_CONF` to enable CONF state.

13. Set `SPI_DMA_SEG_TRAN_DONE_INT_ENA` to enable the `SPI_DMA_SEGTrans_DONE_INT` interrupt. Configure other interrupts if needed according to Section 30.10.

14. Wait for all the slaves to get ready for transfer.

15. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST` and `SPI_RX_AFIFO_RST`, to reset these buffers.

16. Set `SPI_USR` to start this DMA-controlled transfer.

17. Wait for `SPI_DMA_SEGTrans_DONE_INT` interrupt, which means this transfer has finished and the data has been stored into corresponding memory.

**Subheading:**
Configuration of CONF Buffer and Magic Value

**Body Text with Explanation about Magic Values in CONF Buffers:**

In a configurable segmented transfer, only registers which will change from the last transaction (segment) need to be re-configured to new values in CONF state. The configuration of other registers can be skipped (i.e., kept the same) to save time and chip resources.

The first word in GDMA CONF buffer, called `SPI_BIT_MAP_WORD`, defines whether given GP-SPI2 register is to be updated or not in segment. The relation of `SPI_BIT_MAP_WORD` and GP-SPI2 registers to update can be seen in Table 30.5-11 Bitmap (BM) Table. If a bit in the BM table is set to 1, its corresponding register value will be updated in this segment. Registers with corresponding bit set to O remains unchanged.

**Table Title:**
Table 30.5-11. BM Table for CONF State

| BM Bit | Register Name       | BM Bit | Register Name        |
|--------|---------------------|--------|----------------------|
| 0      | SPI_ADDR_REG       | 7      | SPI_MISR_REG         |
| 1      | SPI_CTRL_REG       | 8      | SPI_DIN_MODE_REG     |
| 2      | SPI_CLOCK_REG       | 9      | SPI_DIN_NUM_REG      |
| 3      | SPI_USER_REG        | 10     | SPI_DOUT_MODE_REG    |
| 4      | SPI_USER1_REG       | 11     | SPI_DMA_CONF_REG     |
| 5      | SPI_USER2_REG       | 12     | SPI_DMA_INT_ENA_REG   |
| 6      | SPI_MS_DLEN_REG     | 13     | SPI_DMA_INT_CLR_REG   |

**Additional Information:**

Then new values of all the registers to be modified should be placed right after `SPI_BIT_MAP_WORD`, in consecutive words in the CONF buffer.

To ensure the correctness of the content in each CONF buffer, the value in `SPI_BIT_MAP_WORD[31:28]` is used as “magic value”, and will be compared with `SPI_DMA_SEG MAGIC_VALUE` in register `SPI_SLAVE_REG`. The value of `SPI_DMA_SEG MAGIC_VALUE` should be configured before this DMA-controlled transfer starts, and can not be changed during these segments.

**Footer Information:**
Espressif Systems
1133 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback