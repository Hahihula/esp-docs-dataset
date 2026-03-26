

```markdown
## CONF Buffer Configuration Example

Table 43.5-14 and Table 43.5-15 provide an example to show how to configure a CONF buffer for a transaction (segment) in which SPI_ADDR_REG, SPI_CTRL_REG, SPI_CLOCK_REG, SPI_USER_REG, and SPI_USER1_REG need to be updated.

### Table 43.5-14. An Example of CONF buffer in Segment i

| CONF buffer | Note |
|-------------|------|
| SPI_BIT_MAP_WORD | The first word in this buffer. Its value is 0xA000001F in this example when the SPI_DMA_SEG_MAGIC_VALUE is set to 0xA. As shown in Table 43.5-15, bits 0, 1, 2, 3, and 4 are set, indicating the following registers will be updated. |
| SPI_ADDR_REG | The second word, stores the new value to SPI_ADDR_REG. |
| SPI_CTRL_REG | The third word, stores the new value to SPI_CTRL_REG. |
| SPI_CLOCK_REG | The fourth word, stores the new value to SPI_CLOCK_REG. |
| SPI_USER_REG | The fifth word, stores the new value to SPI_USER_REG. |
| SPI_USER1_REG | The sixth word, stores the new value to SPI_USER1_REG. |

### Table 43.5-15. BM Bit Value and Register to Be Updated in This Example

| BM Bit | Value | Register | BM Bit | Value | Register |
|--------|-------|----------|--------|-------|----------|
| 0      | 1     | SPI_ADDR_REG | 7      | 0     | SPI_MISC_REG |
| 1      | 1     | SPI_CTRL_REG | 8      | 0     | SPI_DIN_MODE_REG |
| 2      | 1     | SPI_CLOCK_REG | 9      | 0     | SPI_DIN_NUM_REG |
| 3      | 1     | SPI_USER_REG | 10     | 0     | SPI_DOUT_MODE_REG |
| 4      | 1     | SPI_USER1_REG | 11     | 0     | SPI_DMA_CONF_REG |
| 5      | 0     | SPI_USER2_REG | 12     | 0     | SPI_DMA_INT_ENA_REG |
| 6      | 0     | SPI_MS_DLEN_REG | 13     | 0     | SPI_DMA_INT_CLR_REG |

## Notes

In a DMA-controlled configurable segmented transfer, please pay special attention to the following bits:
```