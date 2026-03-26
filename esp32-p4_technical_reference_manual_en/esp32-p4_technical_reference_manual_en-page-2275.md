

```markdown
Register 43.14. SPI_DIN_MODE_REG (0x0024)

Continued from the previous page...

SPI_DIN3_MODE Configures the input mode for SPI2HD signal.
0: Input without delay
1: Input at the (SPI_DIN3_NUM + 1)th falling edge of clk_spi_mst
2: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
3: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
Can be configured in CONF state.
(R/W)

SPI_DIN4_MODE Configures the input mode for SPI2D4 signal.
0: Input without delay
1: Input at the (SPI_DIN4_NUM + 1)th falling edge of clk_spi_mst
2: Input at the (SPI_DIN4_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
3: Input at the (SPI_DIN4_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
Can be configured in CONF state.
(R/W)

SPI_DIN5_MODE Configures the input mode for SPI2D5 signal.
0: Input without delay
1: Input at the (SPI_DIN5_NUM + 1)th falling edge of clk_spi_mst
2: Input at the (SPI_DIN5_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
3: Input at the (SPI_DIN5_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
Can be configured in CONF state.
(R/W)

SPI_DIN6_MODE Configures the input mode for SPI2D6 signal.
0: Input without delay
1: Input at the (SPI_DIN6_NUM + 1)th falling edge of clk_spi_mst
2: Input at the (SPI_DIN6_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
3: Input at the (SPI_DIN6_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle
Can be configured in CONF state.
(R/W)

Continued on the next page...
```