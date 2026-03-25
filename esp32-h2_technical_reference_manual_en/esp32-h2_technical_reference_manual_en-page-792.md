

```markdown
| BM Bit | Register Name      | BM Bit | Register Name             |
|--------|--------------------|--------|----------------------------|
| 0      | SPI_ADDR_REG       | 7      | SPI_MISC_REG               |
| 1      | SPI_CTRL_REG       | 8      | SPI_DIN_MODE_REG           |
| 2      | SPI_CLOCK_REG      | 9      | SPI_DIN_NUM_REG            |
| 3      | SPI_USER_REG       | 10     | SPI_DOUT_MODE_REG          |
| 4      | SPI_USER1_REG      | 11     | SPI_DMA_CONF_REG           |
| 5      | SPI_USER2_REG      | 12     | SPI_DMA_INT_ENA_REG        |
| 6      | SPI_MS_DLEN_REG    | 13     | SPI_DMA_INT_CLR_REG        |

Then new values of all the registers to be modified should be placed right after `SPI_BIT_MAP_WORD`, in consecutive words in the CONF buffer.

To ensure the correctness of the content in each CONF buffer, the value in `SPI_BIT_MAP_WORD[31:28]` is used as "magic value", and will be compared with `SPI_DMA_SEG_MAGIC_VALUE` in register `SPI_SLAVE_REG`. The value of `SPI_DMA_SEG_MAGIC_VALUE` should be configured before this DMA-controlled transfer starts, and can not be changed during these segments.

*   If `SPI_BIT_MAP_WORD[31:28] == SPI_DMA_SEG_MAGIC_VALUE`, this DMA-controlled transfer continues normally; the interrupt `SPI_DMA_SEG_TRANS_DONE_INT` is triggered at the end of this DMA-controlled transfer.
*   If `SPI_BIT_MAP_WORD[31:28] != SPI_DMA_SEG_MAGIC_VALUE`, GP-SPI2 state (`spi_st`) goes back to IDLE and the transfer is ended immediately. The interrupt `SPI_DMA_SEG_TRANS_DONE_INT` is still triggered, with `SPI_SEG_MAGIC_ERR_INT_RAW` bit set to 1.

## CONF Buffer Configuration Example

Table 29.5-11 and Table 29.5-12 provide an example to show how to configure a CONF buffer for a transaction (segment i) in which `SPI_ADDR_REG`, `SPI_CTRL_REG`, `SPI_CLOCK_REG`, `SPI_USER_REG`, `SPI_USER1_REG` need to be updated.
```