

```markdown
Register 43.80. LP_SPI_USER1_REG (0x0014)

| Bit | 31 | 27 | 26 | 22 | 21 | 17 | 16 | 15 | 8 | 7 | 0 |
|-----|----|----|----|----|----|----|----|----|---|---|---|
|     |    |    |    | LP_SPI_CS_HOLD_TIME | LP_SPI_USR_ADDR_BITLEN | (reserved) | LP_SPI_MST_WFULL_ERR_END_EN | LP_SPI_CS_SETUP_TIME | LP_SPI_CS_HOLD_TIME | LP_SPI_USR_DUMMY_CYCLELEN |
| Value | 0x1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 7 |

LP_SPI_USR_DUMMY_CYCLELEN Configures the length of DUMMY state.
Measurement unit: SPI_CLK clock cycles.
This value is (the expected cycle number - 1). (R/W)

LP_SPI_MST_WFULL_ERR_END_EN Configures whether or not to end the LP-SPI transfer when SPI RX AFIFO wfull error occurs in master full-/half-duplex transfers.
O: Not end
1: End
(R/W)

LP_SPI_CS_SETUP_TIME Configures the length of prepare (PREP) state.
Measurement unit: SPI_CLK clock cycles.
This value is equal to the expected cycles - 1. This field is used together with LP_SPI_CS_SETUP.
(R/W)

LP_SPI_CS_HOLD_TIME Configures the delay cycles of CS pin.
Measurement unit: SPI_CLK clock cycles.
This field is used together with LP_SPI_CS_HOLD. (R/W)

LP_SPI_USR_ADDR_BITLEN Configures the bit length in address state.
This value is (expected bit number - 1). (R/W)
```