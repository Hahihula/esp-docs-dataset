

```markdown
Register 28.8. SPI_MISC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 0  | Reset |
```

### SPI_CSn_DIS (n = 0 ~ 5)
Configures whether or not to disable SPI_CSn pin. (R/W)

- 0: SPI_CSn signal is from/to SPI_CSn pin.
- 1: Disable SPI_CSn pin.

Can be configured in CONF state.

### SPI_CK_DIS
Configures whether or not to disable SPI_CLK output. (R/W)

- 0: Enable
- 1: Disable

Can be configured in CONF state.

### SPI_MASTER_CS_POL[n]
Configures the polarity of SPI_CSn (n = 0 ~ 5) line in master transfer. (R/W)

- 0: SPI_CSn is low active.
- 1: SPI_CSn is high active.

Can be configured in CONF state.

### SPI_SLAVE_CS_POL
Configures whether or not invert SPI slave input CS polarity. (R/W)

- 0: Not change
- 1: Invert

Can be configured in CONF state.

### SPI_CK_IDLE_EDGE
Configures the level of SPI_CLK line when GP-SPI2 is in idle. (R/W)

- 0: Low
- 1: High

Can be configured in CONF state.

### SPI_CS_KEEP_ACTIVE
Configures whether or not to keep the SPI_CS line low. (R/W)

- 0: Not keep low
- 1: Keep low

Can be configured in CONF state.
```