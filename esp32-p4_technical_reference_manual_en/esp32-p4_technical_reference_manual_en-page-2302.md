

```markdown
Register 43.44. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_Q_POL Configures MISO line polarity.
O: Low
1: High
(R/W)

SPI_D_POL Configures MOSI line polarity.
O: Low
1: High
(R/W)

SPI_HOLD_POL Configures SPI_HOLD output value when SPI is in idle.
O: Output low
1: Output high
(R/W)

SPI_WP_POL Configures the output value of write-protect signal when SPI is in idle.
O: Output low
1: Output high
(R/W)

SPI_RD_BIT_ORDER Configures the bit order in read-data (MISO) state.
O: MSB first
1: LSB first
2: MSB first
3: LSB first
(R/W)

SPI_WR_BIT_ORDER Configures the bit order in command (CMD), address (ADDR), and write-data (MOSI) states.
O: MSB first
1: LSB first
2: MSB first
3: LSB first
(R/W)
```