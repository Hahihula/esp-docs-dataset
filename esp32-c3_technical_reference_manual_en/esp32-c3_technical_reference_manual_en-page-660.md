

```markdown
Register 27.14. SPI_DIN_MODE_REG (0x0024)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 17  |                     |
| 16  |                     |
| 15  |                     |
| 8   | SPI_TIMING_HCLK_ACTIVE |
| 7   | (reserved)          |
| 6   | SPI_DIN3_MODE       |
| 5   | SPI_DIN2_MODE       |
| 4   | SPI_DIN1_MODE       |
| 3   |                     |
| 2   |                     |
| 1   |                     |
| 0   | Reset               |

SPI_DINO_MODE Configure the input mode for FSPID signal. Can be configured in CONF state.
(R/W)

- 0: input without delay
- 1: Input at the (SPI_DINO_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

SPI_DIN1_MODE Configure the input mode for FSPIQ signal. Can be configured in CONF state.
(R/W)

- 0: input without delay
- 1: Input at the (SPI_DIN1_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

SPI_DIN2_MODE Configure the input mode for FSPIWP signal. Can be configured in CONF state.
(R/W)

- 0: input without delay
- 1: Input at the (SPI_DIN2_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Continued on the next page...
```