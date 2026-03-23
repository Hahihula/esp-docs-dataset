

```markdown
Register 27.14. SPI_DIN_MODE_REG (0x0024)

Continued from the previous page...

SPI_DIN3_MODE Configure the input mode for FSPIHD signal. Can be configured in CONF state.
(R/W)

*   0: input without delay
*   1: Input at the (SPI_DIN3_NUM + 1)th falling edge of clk_spi_mst
*   2: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
*   3: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

SPI_TIMING_HCLK_ACTIVE 1: enable HCLK (high-frequency clock) in SPI input timing module. 0: disable HCLK. Can be configured in CONF state. (R/W)
```