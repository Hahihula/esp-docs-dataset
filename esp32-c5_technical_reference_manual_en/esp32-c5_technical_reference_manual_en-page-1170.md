

```markdown
Register 33.8. SPI_MISC_REG (0x0020)

Continued from the previous page...

SPI_CK_DIS Configures whether or not to disable SPI_CLK output.
    0: Enable
    1: Disable
    Can be configured in CONF state.
    (R/W)

SPI_MASTER_CS_POL Configures the polarity of SPI_CSn (n = 0-5) line in master transfer.
    0: SPI_CSn is low active.
    1: SPI_CSn is high active.
    Can be configured in CONF state.
    (R/W)

SPI_CLK_DATA_DTR_EN Reserved (HRO)

SPI_DATA_DTR_EN Reserved (HRO)

SPI_ADDR_DTR_EN Reserved (HRO)

SPI_CMD_DTR_EN Reserved (HRO)

SPI_SLAVE_CS_POL Configures whether or not invert SPI slave input CS polarity.
    0: Not change
    1: Invert
    Can be configured in CONF state.
    (R/W)

Continued on the next page...
```