

```markdown
Register 33.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_D_POL   Configures MOSI line polarity.
    0: Low
    1: High
    Can be configured in CONF state.
    (R/W)

SPI_HOLD_POL   Configures SPI_HOLD output value when SPI is in idle.
    0: Output low
    1: Output high
    Can be configured in CONF state.
    (R/W)

SPI_WP_POL   Configures the output value of write-protect signal when SPI is in idle.
    0: Output low
    1: Output high
    Can be configured in CONF state.
    (R/W)

SPI_RD_BIT_ORDER   Configures the bit order in read-data (MISO) state.
    0: MSB first
    1: LSB first
    Can be configured in CONF state.
    (R/W)

SPI_WR_BIT_ORDER   Configures the bit order in command (CMD), address (ADDR), and write-data (MOSI) states.
    0: MSB first
    1: LSB first
    Can be configured in CONF state.
    (R/W)
```