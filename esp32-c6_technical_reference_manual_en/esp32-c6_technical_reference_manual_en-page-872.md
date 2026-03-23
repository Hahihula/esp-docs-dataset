

```markdown
Register 28.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_RD_BIT_ORDER Configures the bit order in read-data (MISO) state. (R/W)
*   0: MSB first
*   1: LSB first

Can be configured in CONF state.

SPI_WR_BIT_ORDER Configures the bit order in command (CMD), address (ADDR), and write-data (MOSI) states. (R/W)
*   0: MSB first
*   1: LSB first

Can be configured in CONF state.

Register 28.7. SPI_MS_DLEN_REG (0x001C)

SPI_MS_DATA_BITLEN Configures the data bit length of SPI transfer in DMA-controlled master transfer or in CPU-controlled master transfer. Or configures the bit length of SPI RX transfer in DMA-controlled slave transfer. (R/W)
This value shall be (expected bit_num - 1). Can be configured in CONF state.
```