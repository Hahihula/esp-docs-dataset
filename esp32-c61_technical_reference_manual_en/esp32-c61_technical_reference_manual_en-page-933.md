
```markdown
Register 26.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_HOLD_POL Configures SPI_HOLD output value when SPI is in idle.
O: Output low
1: Output high
Can be configured in CONF state.
(R/W)

SPI_WP_POL Configures the output value of write-protect signal when SPI is in idle.
O: Output low
1: Output high
Can be configured in CONF state.
(R/W)

SPI_RD_BIT_ORDER Configures the bit order in read-data (MISO) state.
O: MSB first
1: LSB first
Can be configured in CONF state.
(R/W)

SPI_WR_BIT_ORDER Configures the bit order in command (CMD), address (ADDR), and write-data (MOSI) states.
O: MSB first
1: LSB first
Can be configured in CONF state.
(R/W)

Register 26.7. SPI_MS_DLEN_REG (0x001C)
```