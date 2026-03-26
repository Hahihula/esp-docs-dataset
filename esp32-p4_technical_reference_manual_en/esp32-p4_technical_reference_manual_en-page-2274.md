

```markdown
Register 43.14. SPI_DIN_MODE_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | SPI_TIMING_HCLK_ACTIVE | SPI_DIN7_MODE | SPI_DIN6_MODE | SPI_DIN5_MODE | SPI_DIN4_MODE | SPI_DIN3_MODE | SPI_DIN2_MODE | SPI_DIN1_MODE | SPI_DINO_MODE |
| (reserved) | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SPI_DINO_MODE Configures the input mode for SPI2D signal.
- O: Input without delay
- 1: Input at the (SPI_DINO_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.
(R/W)

SPI_DIN1_MODE Configures the input mode for SPI2Q signal.
- O: Input without delay
- 1: Input at the (SPI_DIN1_NUM+1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.
(R/W)

SPI_DIN2_MODE Configures the input mode for SPI2WP signal.
- O: Input without delay
- 1: Input at the (SPI_DIN2_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.
(R/W)

Continued on the next page...
```