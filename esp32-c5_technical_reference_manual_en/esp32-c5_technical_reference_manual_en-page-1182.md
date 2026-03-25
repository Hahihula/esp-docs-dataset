

```markdown
Register 33.16. SPI_DOUT_MODE_REG (0x002C)

| Bit | Name                  | Description                                                                 |
|-----|-----------------------|-----------------------------------------------------------------------------|
| 31  |                       | (reserved)                                                                  |
| 9   | SPI_DQSMODE           |                                                                             |
| 8   | SPI_DOUT7_MODE        |                                                                             |
| 7   | SPI_DOUT6_MODE        |                                                                             |
| 6   | SPI_DOUT5_MODE        |                                                                             |
| 5   | SPI_DOUT4_MODE        |                                                                             |
| 4   | SPI_DOUT3_MODE        |                                                                             |
| 3   | SPI_DOUT2_MODE        |                                                                             |
| 2   | SPI_DOUT1_MODE        |                                                                             |
| 1   | SPI_DOUT0_MODE        |                                                                             |
| 0   |                       | Reset                                                                        |

SPI_DOUT0_MODE Configures the output mode for FSPID signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge
Can be configured in CONF state.
(R/W)

SPI_DOUT1_MODE Configures the output mode for FSPIQ signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge
Can be configured in CONF state.
(R/W)

SPI_DOUT2_MODE Configures the output mode for FSPIWP signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge
Can be configured in CONF state.
(R/W)

SPI_DOUT3_MODE Configures the output mode for FSPIHD signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge
Can be configured in CONF state.
(R/W)

SPI_DOUT4_MODE Reserved (HRO)
SPI_DOUT5_MODE Reserved (HRO)
SPI_DOUT6_MODE Reserved (HRO)
SPI_DOUT7_MODE Reserved (HRO)
SPI_DQSMODE Reserved (HRO)
```