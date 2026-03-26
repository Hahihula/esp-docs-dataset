

```markdown
Register 43.46. SPI_MISC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  | Reset |

SPI_CSO_DIS Configures whether or not to disable SPI_CSO pin.
- O: SPI_CSO signal is from/to SPI_CSO pin.
- 1: Disable SPI_CSO pin.
(R/W)

SPI_CS1_DIS Configures whether or not to disable SPI_CS1 pin.
- O: SPI_CS1 signal is from/to SPI_CS1 pin.
- 1: Disable SPI_CS1 pin.
(R/W)

SPI_CS2_DIS Configures whether or not to disable SPI_CS2 pin.
- O: SPI_CS2 signal is from/to SPI_CS2 pin.
- 1: Disable SPI_CS2 pin.
(R/W)

SPI_CK_DIS Configures whether or not to disable SPI_CLK output.
- O: Enable
- 1: Disable
(R/W)

SPI_MASTER_CS_POL Configures the polarity of SPI_CSn (n = 0~2) line in master transfer.
- O: SPI_CSn is low active.
- 1: SPI_CSn is high active.
(R/W)

SPI_SLAVE_CS_POL Configures whether or not invert SPI slave input CS polarity.
- O: Not change
- 1: Invert
(R/W)

SPI_CK_IDLE_EDGE Configures the level of SPI_CLK line when GP-SPI3 is in idle.
- O: Low
- 1: High
(R/W)

SPI_CS_KEEP_ACTIVE Configures whether or not to keep the SPI_CS line low.
- O: Not keep low
- 1: Keep low
(R/W)
```