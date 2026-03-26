

```markdown
Register 43.52. SPI_DIN_MODE_REG (0x0024)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 17  | SPI_TIMING_HCLK_ACTIVE |
| 16  |                     |
| 15  |                     |
| 8   | SPI_DIN3_MODE       |
| 7   |                     |
| 6   | SPI_DIN2_MODE       |
| 5   |                     |
| 4   | SPI_DIN1_MODE       |
| 3   |                     |
| 2   | SPI_DINO_MODE       |
| 1   |                     |
| 0   | Reset               |

SPI_DINO_MODE Configures the input mode for SPI3_D signal.
- 0: Input without delay
- 1: Input at the (SPI_DINO_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
(R/W)

SPI_DIN1_MODE Configures the input mode for SPI3_Q signal.
- 0: Input without delay
- 1: Input at the (SPI_DIN1_NUM+1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
(R/W)

SPI_DIN2_MODE Configures the input mode for SPI3_WP signal.
- 0: Input without delay
- 1: Input at the (SPI_DIN2_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
(R/W)

SPI_DIN3_MODE Configures the input mode for SPI3_HD signal.
- 0: Input without delay
- 1: Input at the (SPI_DIN3_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
(R/W)

Continued on the next page...
```