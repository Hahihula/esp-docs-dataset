

```markdown
Chapter 43 SPI Controller (SPI)                                                                 GoBack

Register 43.8. SPI_MISC_REG (0x0020)

Continued from the previous page...

SPI_DQS_IDLE_EDGE   Configured the default value of SPI_DQS.
    0: Low
    1: High
    Can be configured in CONF state.
    (R/W)

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

SPI_QUAD_DIN_PIN_SWAP   Configures whether or not to swap SPI Quad input pins.
    0: Not swap
    1: Swap SPI2D with SPI2Q, and SPI2WP with SPI2HD
    Can be configured in CONF state.
    (R/W)
```