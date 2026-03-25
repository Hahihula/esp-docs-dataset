

```markdown
Register 26.14. SPI_DIN_MODE_REG (0x0024)
```

Continued from the previous page...

```markdown
SPI_DIN4_MODE Configures the delay of input signals relative to the SPI module clock. O: Input without delay 1: Input delayed with the rising edge of clk_apb 2: Input delayed with the falling edge of clk_apb 3: Input delayed with spi_clk Valid only in CONF state. (HRO)
```

```markdown
SPI_DIN5_MODE Configures the delay of input signals relative to the SPI module clock. O: Input without delay 1: Input delayed with the rising edge of clk_apb 2: Input delayed with the falling edge of clk_apb 3: Input delayed with spi_clk Valid only in CONF state. (HRO)
```

```markdown
SPI_DIN6_MODE Configures the delay of input signals relative to the SPI module clock. O: Input without delay 1: Input delayed with the rising edge of clk_apb 2: Input delayed with the falling edge of clk_apb 3: Input delayed with spi_clk Valid only in CONF state. (HRO)
```

```markdown
SPI_DIN7_MODE Configures the delay of input signals relative to the SPI module clock. O: Input without delay 1: Input delayed with the rising edge of clk_apb 2: Input delayed with the falling edge of clk_apb 3: Input delayed with spi_clk Valid only in CONF state. (HRO)
```

```markdown
SPI_TIMING_HCLK_ACTIVE Configures whether or not to enable HCLK (high-frequency clock) in SPI input timing module.
O: Disable
1: Enable
Can be configured in CONF state.
(R/W)
```