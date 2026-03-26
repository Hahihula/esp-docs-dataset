

```markdown
Register 43.54. SPI_DOUT_MODE_REG (0x002C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| ... |                                                                             |
| 4   | SPI_DOUT3_MODE                                                               |
| 3   | SPI_DOUT2_MODE                                                               |
| 2   | SPI_DOUT1_MODE                                                               |
| 1   | SPI_DOUT0_MODE                                                               |
| 0   | Reset                                                                       |

SPI_DOUT0_MODE Configures the output mode for SPI3_D signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge (R/W)

SPI_DOUT1_MODE Configures the output mode for SPI3_Q signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge (R/W)

SPI_DOUT2_MODE Configures the output mode for SPI3_WP signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge (R/W)

SPI_DOUT3_MODE Configures the output mode for SPI3_HD signal.
- 0: Output without delay
- 1: Output with a delay of a SPI module clock cycle at its falling edge (R/W)
```