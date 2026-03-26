

```markdown
Register 43.8. SPI_MISC_REG (0x0020)

Continued from the previous page...

SPI_CK_DIS Configures whether or not to disable SPI_CLK output.
O: Enable
1: Disable
Can be configured in CONF state.
(R/W)

SPI_MASTER_CS_POL Configures the polarity of SPI_CSn (n = 0~5) line in master transfer.
O: SPI_CSn is low active.
1: SPI_CSn is high active.
Can be configured in CONF state.
(R/W)

SPI_CLK_DATA_DTR_EN Configures whether or not to enable DTR mode for SPI_CLK, DATA, and
SPI_DQS when the SPI works as master.
O: Enable DTR mode only for SPI_DQS
1: Enable DTR mode for SPI_CLK, DATA, and SPI_DQS.
This bit should be used with SPI_DATA_DTR_EN, SPI_ADDR_DTR_EN, and SPI_CMD_DTR_EN.
(R/W)

SPI_DATA_DTR_EN Configures whether or not to enable DTR mode for SPI_CLK and DATA in DOUT
and DIN states when the SPI works as master in 1/2/4/8-bit mode.
O: Not enable
1: Enable
Can be configured in CONF state.
(R/W)

SPI_ADDR_DTR_EN Configures whether or not to enable DTR mode for SPI_CLK and DATA in ADDR
state when the SPI works as master in 1/2/4/8-bit mode.
O: Not enable
1: Enable
Can be configured in CONF state.
(R/W)

SPI_CMD_DTR_EN Configures whether or not to enable DTR mode for SPI_CLK and DATA in CMD
state when the SPI works as master in 1/2/4/8-bit mode.
O: Not enable
1: Enable
Can be configured in CONF state.
(R/W)

SPI_SLAVE_CS_POL Configures whether or not to invert SPI slave input CS polarity.
O: Not change
1: Invert
Can be configured in CONF state.
(R/W)
```