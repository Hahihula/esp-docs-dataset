

```markdown
Register 43.92. LP_SPI_DIN_MODE_REG (0x0024)
```

| Bit | Description |
|-----|-------------|
| 17  | (reserved)  |
| 16  | LP_SPI_TIMING_HCLK_ACTIVE |
| 15  | (reserved)  |
| 8   | (reserved)  |
| 7   | (reserved)  |
| 6   | (reserved)  |
| 5   | (reserved)  |
| 4   | LP_SPI_DIN1_MODE |
| 3   | LP_SPI_DINO_MODE |

Reset: `0x00000000`

---

LP_SPI_DINO_MODE Configures the input mode for LP_SPI_D signal.

- 0: Input without delay
- 1: Input at the (LP_SPI_DINO_NUM + 1)th falling edge of clk_spi_mst
- 2: Input at the (LP_SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (LP_SPI_DINO_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

(R/W)

---

LP_SPI_DIN1_MODE Configures the input mode for LP_SPI_Q signal.

- 0: Input without delay
- 1: Input at the (LP_SPI_DIN1_NUM+1)th falling edge of clk_spi_mst
- 2: Input at the (LP_SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst rising edge cycle
- 3: Input at the (LP_SPI_DIN1_NUM + 1)th rising edge of clk_hclk plus one clk_spi_mst falling edge cycle

(R/W)

---

LP_SPI_TIMING_HCLK_ACTIVE Configures whether or not to enable HCLK (high-frequency clock) in LP-SPI input timing module.

- 0: Disable
- 1: Enable

(R/W)
```