

```markdown
Register 33.6. SPI_CTRL_REG (0x0008)

Continued from the previous page...

SPI_FCMD_OCT    Reserved (HRO)

SPI_FREAD_DUAL   Configures whether or not to enable the 2-bit mode of read-data (DIN) state in read operations.
                 O: Disable
                 1: Enable
                 Can be configured in CONF state.
                 (R/W)

SPI_FREAD_QUAD   Configures whether or not to enable the 4-bit mode of read-data (DIN) state in read operations.
                 O: Disable
                 1: Enable
                 Can be configured in CONF state.
                 (R/W)

SPI_FREAD_OCT    Reserved (HRO)

SPI_Q_POL        Configures MSIO line polarity.
                 O: Low
                 1: High
                 Can be configured in CONF state.
                 (R/W)

Continued on the next page...
```