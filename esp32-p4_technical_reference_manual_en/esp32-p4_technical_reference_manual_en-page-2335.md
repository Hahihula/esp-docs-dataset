

```markdown
Register 43.82. LP_SPI_CTRL_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | (reserved) | LP_SPI_WR_BIT_ORDER | LP_SPI_RD_BIT_ORDER | (reserved) | LP_SPI_D_POL | LP_SPI_Q_POL | (reserved) | LP_SPI_DUMMY_OUT | (reserved) |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
```

LP_SPI_DUMMY_OUT Configures whether or not to output the LP_SPI bus signals in DUMMY state.
O: Not output
1: Output
(R/W)

LP_SPI_Q_POL Configures MISO line polarity.
O: Low
1: High
(R/W)

LP_SPI_D_POL Configures MOSI line polarity.
O: Low
1: High
(R/W)

LP_SPI_RD_BIT_ORDER Configures the bit order in read-data (MISO) state.
O: MSB first
1: LSB first
(R/W)

LP_SPI_WR_BIT_ORDER Configures the bit order in command (CMD), address (ADDR), and write-data (MOSI) states.
O: MSB first
1: LSB first
(R/W)
```