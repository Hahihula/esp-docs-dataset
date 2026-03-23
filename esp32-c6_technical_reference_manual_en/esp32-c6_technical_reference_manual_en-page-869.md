

```markdown
Register 28.5. SPI_USER2_REG (0x0018)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 16 | 15 | ... | 0 |
|-----|----|----|----|----|----|----|-----|----|----|-----|---|
|     | SPI_USR_COMMAND_BITLEN | SPI_MST_REMPTY_ERR_END_EN | (reserved) | SPI_USR_COMMAND_VALUE |

SPI_USR_COMMAND_VALUE Configures the command value. (R/W)
Can be configured in CONF state. (R/W)

SPI_MST_REMPTY_ERR_END_EN Configures whether or not to end the SPI transfer when SPI TX AFIFO read empty error occurs in master full-/half-duplex transfers. (R/W)
* 0: Not end
* 1: End

SPI_USR_COMMAND_BITLEN Configures the bit length of command state. (R/W)
This value is (expected bit number - 1). Can be configured in CONF state.
```