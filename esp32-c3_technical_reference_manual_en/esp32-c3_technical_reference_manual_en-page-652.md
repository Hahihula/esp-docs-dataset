

```markdown
Register 27.4. SPI_USER1_REG (0x0014)

| 31 | 27 | 26 | 22 | 21 | 17 | 16 | 15 | 8 | 7 | 0 |
|----|----|----|----|----|----|----|----|---|---|---|
|    |    | SPI_USR_ADDR_BITLEN | SPI_CS_HOLD_TIME | SPI_CS_SETUP_TIME | SPI_MST_WFULL_ERR_END_EN | (reserved) | SPI_USR_DUMMY_CYCLELEN | 23 | 0x1 | 0 |
|    |    |                      |                  |                   |                          |             |                        | Reset |       |       |

SPI_USR_DUMMY_CYCLELEN The length of DUMMY state, in unit of SPI_CLK cycles. This value is (the expected cycle number - 1). Can be configured in CONF state. (R/W)

SPI_MST_WFULL_ERR_END_EN 1: SPI transfer is ended when SPI RX AFIFO wfull error occurs in GP-SPI master full-/half-duplex modes. 0: SPI transfer is not ended when SPI RX AFIFO wfull error occurs in GP-SPI master full-/half-duplex modes. (R/W)

SPI_CS_SETUP_TIME The length of prepare (PREP) state, in unit of SPI_CLK cycles. This value is equal to the expected cycles - 1. This field is used together with SPI_CS_SETUP. Can be configured in CONF state. (R/W)

SPI_CS_HOLD_TIME Delay cycles of CS pin, in units of SPI_CLK cycles. This field is used together with SPI_CS_HOLD. Can be configured in CONF state. (R/W)

SPI_USR_ADDR_BITLEN The bit length in address state. This value is (expected bit number - 1). Can be configured in CONF state. (R/W)
```

```markdown
Register 27.5. SPI_USER2_REG (0x0018)

| 31 | 28 | 27 | 26 | 16 | 15 | 0 |
|----|----|----|----|----|----|---|
|    | SPI_USR_COMMAND_VALUE | SPI_MST_REMPTY_ERR_END_EN | (reserved) | SPI_USR_COMMAND_BITLEN | 7 | 1 | 0x0 | Reset |

SPI_USR_COMMAND_VALUE The value of command. Can be configured in CONF state. (R/W)

SPI_MST_REMPTY_ERR_END_EN 1: SPI transfer is ended when SPI TX AFIFO read empty error occurs in GP-SPI master full-/half-duplex modes. 0: SPI transfer is not ended when SPI TX AFIFO read empty error occurs in GP-SPI master full-/half-duplex modes. (R/W)

SPI_USR_COMMAND_BITLEN The bit length of command state. This value is (expected bit number - 1). Can be configured in CONF state. (R/W)
```