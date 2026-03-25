

```markdown
Register 29.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_D_POL Configures MOSI line polarity.
    0: Low
    1: High
    Can be configured in CONF state. (R/W)

SPI_HOLD_POL Configures SPI_HOLD output value when SPI is in idle.
    0: Output low
    1: Output high
    Can be configured in CONF state. (R/W)

SPI_WP_POL Configures the output value of write-protect signal when SPI is in idle.
    0: Output low
    1: Output high
    Can be configured in CONF state. (R/W)

SPI_RD_BIT_ORDER Configures the bit order in read-data (MISO) state.
    0: MSB first
    1: LSB first
    Can be configured in CONF state. (R/W)

SPI_WR_BIT_ORDER Configures the bit order in command (CMD), address (ADDR), and write-data (MOSI) states.
    0: MSB first
    1: LSB first
    Can be configured in CONF state. (R/W)

Register 29.7. SPI_MS_DLEN_REG (0x001C)
```

```markdown
| Bit | Description         |
|-----|---------------------|
| 31  | reserved            |
| 18  |                     |
| 17  |                     |
| 0   | Reset               |

SPI_MS_DATA_BITLEN Configures the data bit length of SPI transfer in DMA-controlled master transfer or in CPU-controlled master transfer. Or configures the bit length of SPI RX transfer in DMA-controlled slave transfer.
This value shall be (expected bit_num - 1). Can be configured in CONF state. (R/W)
```