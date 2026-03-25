

```markdown
Register 29.6. SPI_CTRL_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | SPI_WR_BIT_ORDER | SPI_RD_BIT_ORDER | reserved | SPI_WP_POL | SPI_HOLD_POL | SPI_D_POL | SPI_O_POL | (reserved) | SPI_FREAD_QUAD | SPI_FREAD_DUAL | reserved | SPI_FCMD_QUAD | FOMD_DUAL | (reserved) | SPI_FADDR_QUAD | SPI_FADDR_DUAL | (reserved) | SPI_DUMMY_OUT | (reserved) |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SPI_DUMMY_OUT Configures whether or not to output the FSPI bus signals in DUMMY state.
O: Not output
1: Output
Can be configured in CONF state. (R/W)

SPI_FADDR_DUAL Configures whether or not to enable 2-bit mode during address (ADDR) state.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_FADDR_QUAD Configures whether or not to enable 4-bit mode during address (ADDR) state.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_FCMD_DUAL Configures whether or not to enable 2-bit mode during command (CMD) state.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_FCMD_QUAD Configures whether or not to enable 4-bit mode during command (CMD) state.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_FREAD_DUAL Configures whether or not to enable the 2-bit mode of read-data (DIN) state in read operations.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_FREAD_QUAD Configures whether or not to enable the 4-bit mode of read-data (DIN) state in read operations.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_Q_POL Configures MSIO line polarity.
O: Low
1: High
Can be configured in CONF state. (R/W)
```