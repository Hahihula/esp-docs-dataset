

```markdown
Register 43.50. SPI_CLOCK_REG (0x000C)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|    | SPI_CLK_EQU_SYSCLK | (reserved) | SPI_CLKDIV_PRE | SPI_CLKCNT_N | SPI_CLKCNT_H | SPI_CLKCNT_L |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x3 | 0x1 | 0x3 | Reset |

SPI_CLKCNT_L Configures clock duty cycles, together with SPI_CLKCNT_H and SPI_CLKCNT_N.
In master transfer, this field must be equal to SPI_CLKCNT_N.
In slave mode, it must be 0.
Can be configured in CONF state.
(R/W)

SPI_CLKCNT_H Configures the duty cycle of SPI_CLK (high level) in master transfer.
It's recommended to configure this value to floor((SPI_CLKCNT_N + 1)/2 - 1). floor() here is to round a number down, e.g., floor(2.2) = 2.
In slave mode, it must be 0.
(R/W)

SPI_CLKCNT_N Configures the divider of SPI_CLK in master transfer.
SPI_CLK frequency is f_clk_spi_mst/(SPI_CLKDIV_PRE + 1)/(SPI_CLKCNT_N + 1).
(R/W)

SPI_CLKDIV_PRE Configures the pre-divider of SPI_CLK in master transfer.
(R/W)

SPI_CLK_EQU_SYSCLK Configures whether or not the SPI_CLK is equal to clk_spi_mst in master transfer.
0: SPI_CLK is divided from clk_spi_mst.
1: SPI_CLK is equal to clk_spi_mst.
(R/W)

Register 43.51. SPI_CLK_GATE_REG (0x00E8)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|    | (reserved) | SPI_CLK_EN |
| 0 | 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SPI_CLK_EN Configures whether or not to enable clock gate.
0: Disable
1: Enable
(R/W)
```