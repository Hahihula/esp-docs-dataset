

```markdown
Register 33.8. SPI_MISC_REG (0x0020)

Continued from the previous page...

SPI_DQS_IDLE_EDGE    Reserved (HRO)

SPI_CK_IDLE_EDGE     Configures the level of SPI_CLK line when GP-SPI2 is in idle.
    0: Low
    1: High
    Can be configured in CONF state.
    (R/W)

SPI_CS_KEEP_ACTIVE   Configures whether or not to keep the SPI_CS line low.
    0: Not keep low
    1: Keep low
    Can be configured in CONF state.
    (R/W)

SPI_QUAD_DIN_PIN_SWAP Configures whether or not to swap SPI Quad input pins.
    0: Not swap
    1: Swap FSPID with FSPIQ, and FSPIWP with FSPIHD
    Can be configured in CONF state.
    (R/W)
```