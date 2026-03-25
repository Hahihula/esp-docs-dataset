

```markdown
Register 26.5. SPI_USER2_REG (0x0018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SPI_USR_COMMAND_BITLEN | SPI_MST_REMPTY_ERR_END_EN | (reserved) | SPI_USR_COMMAND_VALUE |
| 7   | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SPI_USR_COMMAND_VALUE Configures the command value.
Can be configured in CONF state.
(R/W)

SPI_MST_REMPTY_ERR_END_EN Configures whether or not to end the SPI transfer when SPI TX AFIFO read empty error occurs in master full-/half-duplex transfers.
0: Not end
1: End
(R/W)

SPI_USR_COMMAND_BITLEN Configures the bit length of command state.
This value is (expected bit number - 1).
Can be configured in CONF state.
(R/W)
```