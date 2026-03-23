

```markdown
Register 28.14. SPI_DIN_MODE_REG (0x0024)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 17  |                     |
| 16  |                     |
| 15  | SPI_TIMING_HCLK_ACTIVE |
|     | (reserved)          |
| 8   | SPI_DIN3_MODE       |
| 7   |                     |
| 6   |                     |
| 5   |                     |
| 4   |                     |
| 3   | SPI_DIN2_MODE       |
| 2   |                     |
| 1   | SPI_DIN1_MODE       |
| 0   | SPI_DINO_MODE       |

Reset: All bits are 0.

---

SPI_DINO_MODE Configures the input mode for FSPID signal. (R/W)

- 0: Input without delay
- 1: Input at the (SPI_DINO_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.

---

SPI_DIN1_MODE Configures the input mode for FSPIQ signal. (R/W)

- 0: Input without delay
- 1: Input at the (SPI_DIN1_NUM+1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.

---

SPI_DIN2_MODE Configures the input mode for FSPIWP signal. (R/W)

- 0: Input without delay
- 1: Input at the (SPI_DIN2_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (SPI_DIN2_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

Can be configured in CONF state.

---

Continued on the next page...
```