

```markdown
Register 26.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_FCMD_OCT   Configures whether or not to enable 8-bit mode during command (CMD) state.
               0: Disable
               1: Enable
               Can be configured in CONF state.
               (HRO)

SPI_FREAD_DUAL  Configures whether or not to enable the 2-bit mode of read-data (DIN) state in
               read operations.
               0: Disable
               1: Enable
               Can be configured in CONF state.
               (R/W)

SPI_FREAD_QUAD  Configures whether or not to enable the 4-bit mode of read-data (DIN) state in
               read operations.
               0: Disable
               1: Enable
               Can be configured in CONF state.
               (R/W)

SPI_FREAD_OCT   Configures whether or not to enable the 8-bit mode of read-data (DIN) state in
               read operations.
               0: Disable
               1: Enable
               Can be configured in CONF state.
               (HRO)

SPI_Q_POL       Configures MISO line polarity.
               0: Low
               1: High
               Can be configured in CONF state.
               (R/W)

SPI_D_POL       Configures MOSI line polarity.
               0: Low
               1: High
               Can be configured in CONF state.
               (R/W)

Continued on the next page...
```