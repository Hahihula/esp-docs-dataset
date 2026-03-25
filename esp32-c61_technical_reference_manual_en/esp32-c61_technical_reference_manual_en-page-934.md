

```markdown
Register 26.8. SPI_MISC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SPI_QUAD_DIN_PIN_SWAP | SPI_CS_KEEP_ACTIVE | SPI_CLK_IDLE_EDGE | (reserved) | SPI_DQS_IDLE_EDGE | (reserved) | SPI_CMD_DTR_EN | SPI_ADDR_DTR_EN | SPI_DATA_DTR_EN | SPI_CLK_DATA_DTR_EN | (reserved) | SPI_MASTER_CS_POL | SPI_OK_DIS | SPI_CS5_DIS | SPI_CS4_DIS | SPI_CS3_DIS | SPI_CS2_DIS | SPI_CS1_DIS | SPI_CS0_DIS | Reset |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 0 |

SPI_CSn_DIS Configures whether or not to disable SPI_CSn pin. (N=0~5)
O: SPI_CSn signal is from/to SPI_CSn pin.
1: Disable SPI_CSn pin.
Can be configured in CONF state.
(R/W)

SPI_CK_DIS Configures whether to disable SPI_CLK output.
O: Enable
1: Disable
Can be configured in CONF state.
(R/W)

SPI_MASTER_CS_POL Configures the polarity of SPI_CSn (n = 0-5) line in master transfer.
O: SPI_CSn is low active.
1: SPI_CSn is high active.
Can be configured in CONF state.
(R/W)

SPI_CLK_DATA_DTR_EN Configures whether to enable DTR mode for SPI_CLK, DATA, and SPI_DQS when SPI works as master.
O: Enable DTR mode only for SPI_DQS
1: Enable DTR mode for SPI_CLK, DATA, and SPI_DQS.
This bit should be used with SPI_DATA_DTR_EN, SPI_ADDR_DTR_EN, and SPI_CMD_DTR_EN.
(HRO)

SPI_DATA_DTR_EN Configures whether to enable DTR mode for SPI_CLK and DATA in DOUT and DIN states when the SPI works as master in 1/2/4/8-bit mode.
O: Not enable
1: Enable
Can be configured in CONF state.
(HRO)

SPI_ADDR_DTR_EN Configures whether or not to enable DTR mode for SPI_CLK and DATA in ADDR state when the SPI works as master in 1/2/4/8-bit mode.
O: Not enable
1: Enable
Can be configured in CONF state.
(HRO)
```