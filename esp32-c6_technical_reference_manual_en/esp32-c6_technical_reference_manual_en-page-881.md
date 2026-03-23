

```markdown
Register 28.14. SPI_DIN_MODE_REG (0x0024)

Continued from the previous page...

SPI_DIN3_MODE Configures the input mode for FSPIHD signal. (R/W)

*   0: Input without delay
*   1: Input at the (SPI_DIN3_NUM + 1)th falling edge of clk_spi_mst
*   2: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
*   3: Input at the (SPI_DIN3_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.

SPI_TIMING_HCLK_ACTIVE Configures whether or not to enable HCLK (high-frequency clock) in SPI input timing module. (R/W)

*   0: Disable
*   1: Enable

Can be configured in CONF state.
```