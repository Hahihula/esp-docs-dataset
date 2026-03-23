

```markdown
Register 27.8. SPI_MISC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 24 | 23 | 22 | ... | 13 | 12 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|-----|----|----|---|---|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | ... | ... | 0 | 1 | 1 | 1 | 1 | 1 | 1 | Reset |

SPI_CSO_DIS SPI CSO pin enable bit. 1: disable CSO, 0: SPI_CSO signal is from/to CSO pin. Can be configured in CONF state. (R/W)

SPI_CS1_DIS SPI CS1 pin enable bit. 1: disable CS1, 0: SPI_CS1 signal is from/to CS1 pin. Can be configured in CONF state. (R/W)

SPI_CS2_DIS SPI CS2 pin enable bit. 1: disable CS2, 0: SPI_CS2 signal is from/to CS2 pin. Can be configured in CONF state. (R/W)

SPI_CS3_DIS SPI CS3 pin enable bit. 1: disable CS3, 0: SPI_CS3 signal is from/to CS3 pin. Can be configured in CONF state. (R/W)

SPI_CS4_DIS SPI CS4 pin enable bit. 1: disable CS4, 0: SPI_CS4 signal is from/to CS4 pin. Can be configured in CONF state. (R/W)

SPI_CS5_DIS SPI CS5 pin enable bit. 1: disable CS5, 0: SPI_CS5 signal is from/to CS5 pin. Can be configured in CONF state. (R/W)

SPI_CLK_DIS 1: disable SPI_CLK output. 0: enable SPI_CLK output. Can be configured in CONF state. (R/W)

SPI_MASTER_CS_POL In master mode, the bits are the polarity of SPI CS line, the value is equivalent to SPI_CS ^ SPI_MASTER_CS_POL. Can be configured in CONF state. (R/W)

SPI_SLAVE_CS_POL Configure SPI slave input CS polarity. 1: invert. 0: not change. Can be configured in CONF state. (R/W)

SPI_CK_IDLE_EDGE 1: SPI_CLK line is high when GP-SPI2 is in idle. 0: SPI_CLK line is low when GP-SPI2 is in idle. Can be configured in CONF state. (R/W)

SPI_CS_KEEP_ACTIVE SPI CS line keeps low when the bit is set. Can be configured in CONF state. (R/W)

SPI_QUAD_DIN_PIN_SWAP 1: SPI quad input swap enable. 0: SPI quad input swap disable. Can be configured in CONF state. (R/W)
```