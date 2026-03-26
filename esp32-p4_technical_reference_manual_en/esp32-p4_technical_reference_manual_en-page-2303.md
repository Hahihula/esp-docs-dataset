

```markdown
Register 43.45. SPI_MS_DLEN_REG (0x001C)
```

| Bit Field | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31-18     | (reserved)                                                                  |
| 17        | SPI_MS_DATA_BITLEN                                                          |
|           |                                                                             |
| Reset     | 0                                                                           |

**SPI_MS_DATA_BITLEN** Configures the data bit length of SPI transfer in CPU-controlled master transfer. Or configures the bit length of SPI RX transfer in DMA-controlled slave transfer. This value shall be (expected bit_num - 1).  
(R/W)
```