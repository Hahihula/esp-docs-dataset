

```markdown
Register 33.8. SPI_MISC_REG (0x0020)

| 31 | 30 | 29 | 28 | 25 | 24 | 23 | 22 | 20 | 19 | 18 | 17 | 16 | 15 | 13 | 12 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|
|    | SPI_QUAD_DIN_PIN_SWAP<br>SPI_CS_KEEP_ACTIVE<br>SPI_CLK_IDLE_EDGE | (reserved) | SPI_DQS_IDLE_EDGE<br>SPI_SLAVE_CS_POL | (reserved) | SPI_CMD_DTR_EN<br>SPI_ADDR_DTR_EN<br>SPI_DATA_DTR_EN<br>SPI_CLK_DATA_DTR_EN | (reserved) | SPI_MASTER_CS_POL<br>SPI_OK_DIS<br>SPI_CS5_DIS<br>SPI_CS4_DIS<br>SPI_CS3_DIS<br>SPI_CS2_DIS<br>SPI_CS1_DIS<br>SPI_CS0_DIS |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 0 |

SPI_CS0_DIS Configures whether or not to disable SPI_CS0 pin.
0: SPI_CS0 signal is from/to SPI_CS0 pin.
1: Disable SPI_CS0 pin.
Can be configured in CONF state.
(R/W)

SPI_CS1_DIS Configures whether or not to disable SPI_CS1 pin.
0: SPI_CS1 signal is from/to SPI_CS1 pin.
1: Disable SPI_CS1 pin.
Can be configured in CONF state.
(R/W)

SPI_CS2_DIS Configures whether or not to disable SPI_CS2 pin.
0: SPI_CS2 signal is from/to SPI_CS2 pin.
1: Disable SPI_CS2 pin.
Can be configured in CONF state.
(R/W)

SPI_CS3_DIS Configures whether or not to disable SPI_CS3 pin.
0: SPI_CS3 signal is from/to SPI_CSn pin.
1: Disable SPI_CS3 pin.
Can be configured in CONF state.
(R/W)

SPI_CS4_DIS Configures whether or not to disable SPI_CS4 pin.
0: SPI_CS4 signal is from/to SPI_CS4 pin.
1: Disable SPI_CS4 pin.
Can be configured in CONF state.
(R/W)

SPI_CS5_DIS Configures whether or not to disable SPI_CS5 pin.
0: SPI_CS5 signal is from/to SPI_CS5 pin.
1: Disable SPI_CS5 pin.
Can be configured in CONF state.
(R/W)
```