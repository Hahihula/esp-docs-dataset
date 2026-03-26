

```markdown
Register 43.83. LP_SPI_MS_DLEN_REG (0x001C)
```

| 31 | 18 | 17 | ... | 0 |
|----:|----:|----:|-----|---|
| 0  | 0  | 0  | ... | Reset |

LP_SPI_MS_DATA_BITLEN Configures the data bit length of SPI transfer in CPU-controlled master transfer.

This value shall be (expected bit_num - 1).

(R/W)
```