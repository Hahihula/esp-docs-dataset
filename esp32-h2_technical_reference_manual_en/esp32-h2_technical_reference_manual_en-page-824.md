

```markdown
Register 29.14. SPI_DIN_MODE_REG (0x0024)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 17  | SPI_TIMING_HCLK_ACTIVE |
| 16  | (reserved)          |
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

SPI_DINO_MODE Configures the input mode for FSPID signal.
- 0: Input without delay
- 1: Input at the (SPI_DINO_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state. (R/W)

SPI_DIN1_MODE Configures the input mode for FSPIQ signal.
- 0: Input without delay
- 1: Input at the (SPI_DIN1_NUM+1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state. (R/W)

SPI_DIN2_MODE Configures the input mode for FSPIWP signal.
- 0: Input without delay
- 1: Input at the (SPI_DIN2_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state. (R/W)

SPI_DIN3_MODE Configures the input mode for FSPIHD signal.
- 0: Input without delay
- 1: Input at the (SPI_DIN3_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state. (R/W)

Continued on the next page...
```