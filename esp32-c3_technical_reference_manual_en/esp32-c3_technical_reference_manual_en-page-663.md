

```markdown
Register 27.16. SPI_DOUT_MODE_REG (0x002C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 4   | SPI_DOUT3_MODE                                                               |
| 3   | SPI_DOUT2_MODE                                                               |
| 2   | SPI_DOUT1_MODE                                                               |
| 1   | SPI_DOUT0_MODE                                                               |
| 0   | Reset                                                                       |

SPI_DOUT0_MODE Configure the output mode for FSPID signal. Can be configured in CONF state. (R/W)
- 0: output without delay
- 1: output with a delay of a SPI module clock cycle at its falling edge

SPI_DOUT1_MODE Configure the output mode for FSPIQ signal. Can be configured in CONF state. (R/W)
- 0: output without delay
- 1: output with a delay of a SPI module clock cycle at its falling edge

SPI_DOUT2_MODE Configure the output mode for FSPIDWP signal. Can be configured in CONF state. (R/W)
- 0: output without delay
- 1: output with a delay of a SPI module clock cycle at its falling edge

SPI_DOUT3_MODE Configure the output mode for FSPIHD signal. Can be configured in CONF state. (R/W)
- 0: output without delay
- 1: output with a delay of a SPI module clock cycle at its falling edge
```