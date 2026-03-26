

```markdown
Register 43.90. LP_SPI_CLOCK_REG (0x0000C)
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | O | 0x3 | Ox1 | 0x3 | Reset |

LP_SPI_CLKCNT_L Configures clock duty cycles, together with LP_SPI_CLKCNT_H and LP_SPI_CLKCNT_N.
In master transfer, this field must be equal to LP_SPI_CLKCNT_N.
In slave mode, it must be 0.
(R/W)

LP_SPI_CLKCNT_H Configures the duty cycle of LP_SPI_CLK (high level) in master transfer.
It's recommended to configure this value to floor((LP_SPI_CLKCNT_N + 1)/2 - 1). floor() here is to round a number down, e.g., floor(2.2) = 2.
In slave mode, it must be 0.
(R/W)

LP_SPI_CLKCNT_N Configures the divider of LP_SPI_CLK in master transfer.
LP_SPI_CLK frequency is f_lp_spi_pclk/(LP_SPI_CLKDIV_PRE + 1)/(LP_SPI_CLKCNT_N + 1).
(R/W)

LP_SPI_CLKDIV_PRE Configures the pre-divider of LP_SPI_CLK in master transfer.
(R/W)

LP_SPI_CLK_EQU_SYSCLK Configures whether or not the LP_SPI_CLK is equal to lp_spi_pclk in master transfer.

0: LP_SPI_CLK is divided from lp_spi_pclk.
1: LP_SPI_CLK is equal to lp_spi_pclk.
(R/W)
```

```markdown
Register 43.91. LP_SPI_CLK_GATE_REG (0x00E8)
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

LP_SPI_CLK_EN Configures whether or not to enable clock gate.

0: Disable
1: Enable
(R/W)
```