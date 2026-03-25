

```markdown
Register 26.8. SPI_MISC_REG (0x0020)

Continued from the previous page...

SPI_CMD_DTR_EN Configures whether or not to enable DTR mode for SPI_CLK and DATA in CMD state when the SPI works as master in 1/2/4/8-bit mode.
O: Not enable
1: Enable
Can be configured in CONF state.
(HRO)

SPI_SLAVE_CS_POL Configures whether or not invert SPI slave input CS polarity.
O: Not change
1: Invert
Can be configured in CONF state.
(R/W)

SPI_DQS_IDLE_EDGE Configures the default value of SPI_DQS.
O: Low
1: High
Can be configured in CONF state.
(HRO)

SPI_CK_IDLE_EDGE Configures the level of SPI_CLK line when GP-SPI2 is in idle.
O: Low
1: High
Can be configured in CONF state.
(R/W)

SPI_CS_KEEP_ACTIVE Configures whether or not to keep the SPI_CS line low.
O: Not keep low
1: Keep low
Can be configured in CONF state.
(R/W)

Continued on the next page...

Register 26.8. SPI_MISC_REG (0x0020)

Continued from the previous page...

SPI_QUAD_DIN_PIN_SWAP Configures whether to swap SPI QAUD input pins.
O: disable the swap
1: Swap FSPID with FSPIQ, and FSPIWP with FSPIHD
Can be configured in CONF state.
(R/W)
```