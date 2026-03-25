

```markdown
Chapter 33 SPI Controller (SPI)

Register 33.7. SPI_MS_DLEN_REG (0x001C)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 18-17 | SPI_MS_DATA_BITLEN |

```markdown
SPI_MS_DATA_BITLEN Configures the data bit length of SPI transfer in DMA-controlled master transfer or in CPU-controlled master transfer. Or configures the bit length of SPI RX transfer in DMA-controlled slave transfer.
This value shall be (expected bit_num - 1).
Can be configured in CONF state.
(R/W)
```