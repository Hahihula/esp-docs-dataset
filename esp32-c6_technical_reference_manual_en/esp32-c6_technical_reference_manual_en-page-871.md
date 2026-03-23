

```markdown
Register 28.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_FREAD_DUAL Configures whether or not to enable the 2-bit mode of read-data (DIN) state in read operations. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_FREAD_QUAD Configures whether or not to enable the 4-bit mode of read-data (DIN) state in read operations. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_Q_POL Configures MISO line polarity. (R/W)
*   0: Low
*   1: High

Can be configured in CONF state.

SPI_D_POL Configures MOSI line polarity. (R/W)
*   0: Low
*   1: High

Can be configured in CONF state.

SPI_HOLD_POL Configures SPI_HOLD output value when SPI is in idle. (R/W)
*   0: Output low
*   1: Output high

Can be configured in CONF state.

SPI_WP_POL Configures the output value of write-protect signal when SPI is in idle. (R/W)
*   0: Output low
*   1: Output high

Can be configured in CONF state.

Continued on the next page...
```