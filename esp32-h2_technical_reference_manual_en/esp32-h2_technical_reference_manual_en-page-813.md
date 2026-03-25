

```markdown
Register 29.4. SPI_USER1_REG (0x0014)

| 31 | 27 | 26 | 22 | 21 | 17 | 16 | 15 | 8 | 7 | 0 |
|----|----|----|----|----|----|----|----|---|---|---|
|    |    | SPI_USR_ADDR_BITLEN | SPI_CS_HOLD_TIME | SPI_CS_SETUP_TIME | SPI_MST_WFULL_ERR_END_EN | (reserved) | SPI_USR_DUMMY_CYCLELEN |
| 23 | 0x1 | 0 | 1 | 0 | 0 | 0 | 0 | 7 | Reset |

SPI_USR_DUMMY_CYCLELEN Configures the length of DUMMY state.
Measurement unit: SPI_CLK clock cycles.
This value is (the expected cycle number - 1). Can be configured in CONF state. (R/W)

SPI_MST_WFULL_ERR_END_EN Configures whether or not to end the SPI transfer when SPI RX AFIFO wfull error occurs in master full-/half-duplex transfers.
0: Not end
1: End
(R/W)

SPI_CS_SETUP_TIME Configures the length of prepare (PREP) state.
Measurement unit: SPI_CLK clock cycles.
This value is (the expected cycles - 1). This field is used together with SPI_CS_SETUP. Can be configured in CONF state. (R/W)

SPI_CS_HOLD_TIME Configures the delay cycles of CS pin.
Measurement unit: SPI_CLK clock cycles.
This field is used together with SPI_CS_HOLD. Can be configured in CONF state. (R/W)

SPI_USR_ADDR_BITLEN Configures the bit length in address state.
This value is (expected bit number - 1). Can be configured in CONF state. (R/W)
```