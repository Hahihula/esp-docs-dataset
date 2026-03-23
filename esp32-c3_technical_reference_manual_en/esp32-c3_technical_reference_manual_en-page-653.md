

```markdown
Register 27.6. SPI_CTRL_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | SPI_WR_BIT_ORDER | SPI_RD_BIT_ORDER | reserved | SPI_WP_POL | SPI_HOLD_POL | SPI_D_POL | SPI_Q_POL | (reserved) | SPI_FREAD_QUAD | SPI_FREAD_DUAL | reserved | SPI_FCMD_QUAD | FOMD_DUAL | reserved | SPI_FADDR_QUAD | SPI_FADDR_DUAL | reserved | SPI_DUMMY_OUT | Reset |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
```

SPI_DUMMY_OUT Configure the output signal level in DUMMY state. Can be configured in CONF state. (R/W)

SPI_FADDR_DUAL Apply 2-bit mode during address (ADDR) state. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_FADDR_QUAD Apply 4-bit mode during address (ADDR) state. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_FCMD_DUAL Apply 2-bit mode during command (CMD) state. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_FCMD_QUAD Apply 4-bit mode during command (CMD) state. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_FREAD_DUAL In read operations, read-data (DIN) state is in 2-bit mode. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_FREAD_QUAD In read operations, read-data (DIN) state is in 4-bit mode. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_Q_POL This bit is used to set MISO line polarity. 1: high; 0: low. Can be configured in CONF state. (R/W)

SPI_D_POL This bit is used to set MOSI line polarity. 1: high; 0: low. Can be configured in CONF state. (R/W)

SPI_HOLD_POL This bit is used to set SPI_HOLD output value when SPI is in idle. 1: output high; 0: output low. Can be configured in CONF state. (R/W)

SPI_WP_POL This bit is to set the output value of write-protect signal when SPI is in idle. 1: output high; 0: output low. Can be configured in CONF state. (R/W)

SPI_RD_BIT_ORDER In read-data (MISO) state, 1: LSB first; 0: MSB first. Can be configured in CONF state. (R/W)

SPI_WR_BIT_ORDER In command (CMD), address (ADDR), and write-data (MOSI) states, 1: LSB first; 0: MSB first. Can be configured in CONF state. (R/W)
```