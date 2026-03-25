
```markdown
## Configuration of CONF Buffer and Magic Value

In a configurable segmented transfer, only registers which change from the last transaction (segment) need to be re-configured to new values in CONF state. The configuration of other registers can be skipped (i.e., kept the same) to save time and chip resources.

The first word in GDMA CONF buffer, called SPI_BIT_MAP_WORD, defines whether given GP-SPI2 register is to be updated or not in segment i. The relation of SPI_BIT_MAP_WORD and GP-SPI2 registers to update can be seen in Table 33.5-10 Bitmap (BM) Table. If a bit in the BM table is set to 1, its corresponding register value will be updated in this segment. Otherwise, if some registers should be kept from being changed, the related bits should be set to 0.

Table 33.5-10. BM Table for CONF State

| BM Bit | Register         | BM Bit | Register               |
|--------|------------------|--------|------------------------|
| 0      | SPI_ADDR_REG     | 7      | SPI_MISC_REG           |
| 1      | SPI_CTRL_REG     | 8      | SPI_DIN_MODE_REG       |
| 2      | SPI_CLOCK_REG    | 9      | SPI_DIN_NUM_REG        |
| 3      | SPI_USER_REG     | 10     | SPI_DOUT_MODE_REG      |
| 4      | SPI_USER1_REG    | 11     | SPI_DMA_CONF_REG       |
| 5      | SPI_USER2_REG    | 12     | SPI_DMA_INT_ENA_REG    |
| 6      | SPI_MS_DLEN_REG  | 13     | SPI_DMA_INT_CLR_REG    |

Then new values of all the registers to be modified should be placed right after SPI_BIT_MAP_WORD, in consecutive words in the CONF buffer.

To ensure the correctness of the content in each CONF buffer, the value in SPI_BIT_MAP_WORD[31:28] is used as a "magic value", and will be compared with SPI_DMA_SEG_MAGIC_VALUE in register SPI_SLAVE_REG. The value of SPI_DMA_SEG_MAGIC_VALUE should be configured before this DMA-controlled transfer starts, and can not be changed during these segments.

* If SPI_BIT_MAP_WORD[31:28] == SPI_DMA_SEG_MAGIC_VALUE, this DMA-controlled transfer continues normally. SPI_DMA_SEG_TRANS_DONE_INT is triggered at the end of this DMA-controlled transfer.
* If SPI_BIT_MAP_WORD[31:28] != SPI_DMA_SEG_MAGIC_VALUE, GP-SPI2 state (spi_st) goes back to IDLE and the transfer is ended immediately. The interrupt SPI_DMA_SEG_TRANS_DONE_INT is still triggered, with SPI_SEG_MAGIC_ERR_INT_RAW bit set to 1.

## CONF Buffer Configuration Example

Table 33.5-11 and Table 33.5-12 provide an example to configure a CONF buffer for a transaction (segment) in which SPI_ADDR_REG, SPI_CTRL_REG, SPI_CLOCK_REG, SPI_USER_REG, and SPI_USER1_REG need to be updated.

Table 33.5-11. An Example of CONF buffer i in Segment i

| CONF buffer i | Note |
|---------------|------|
| SPI_BIT_MAP_WORD | The first word in this buffer. Its value is 0xA000001F in this example when the SPI_DMA_SEG_MAGIC_VALUE is set to 0xA. As shown in Table 33.5-12, bits 0, 1, 2, 3, and 4 are set, indicating the following registers will be updated. |
```