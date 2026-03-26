

```markdown
Chapter 43 SPI Controller (SPI)

Register 43.1. SPI_CMD_REG (0x0000)
| 31 | 25 | 24 | 23 | 22 | 21 | 18 | 17 |
|----|----|----|----|----|----|----|----|
|    | SPI_USR | SPI_UPDATE | (reserved) | SPI_CONF_BITLEN | Reset |

SPI_CONF_BITLEN Configures the SPI_CLK cycles of SPI CONF state.
Measurement unit: SPI_CLK clock cycle.
Can be configured in CONF state.
(R/W)

SPI_UPDATE Configures whether or not to synchronize SPI registers from APB clock domain into
SPI module clock domain.
0: Not synchronize
1: Synchronize
This bit is only used in SPI master transfer.
(WT)

SPI_USR Configures whether or not to enable user-defined command.
0: Not enable
1: Enable
An SPI operation will be triggered when the bit is set. This bit will be cleared once the operation
is done. Can not be changed by CONF_buf.
(R/W/SC)

Register 43.2. SPI_ADDR_REG (0x0004)
| 31 | 0 |
|----|----|
|    | Reset |

SPI_USR_ADDR_VALUE Configures the address to slave. Can be configured in CONF state.
(R/W)
```