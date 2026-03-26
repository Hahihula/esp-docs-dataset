

```markdown
Register 43.81. LP_SPI_USER2_REG (0x0018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 |
|-----|----|----|----|----|----|----|-----|----|----|----|----|----|----|----|---|---|---|
|     |    |    |    | LP_SPI_USR_COMMAND_BITLEN | LP_SPI_MST_REMPTY_ERR_END_EN | (reserved) | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
```

LP_SPI_USR_COMMAND_VALUE Configures the command value. (R/W)

LP_SPI_MST_REMPTY_ERR_END_EN Configures whether or not to end the LP-SPI transfer when SPI TX AFIFO read empty error occurs in master full-/half-duplex transfers.

O: Not end  
1: End  
(R/W)

LP_SPI_USR_COMMAND_BITLEN Configures the bit length of command state. This value is (expected bit number - 1). (R/W)
```