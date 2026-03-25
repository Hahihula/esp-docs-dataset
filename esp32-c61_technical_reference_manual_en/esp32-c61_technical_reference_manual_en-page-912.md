

```markdown
Figure 26.6-1 and Figure 26.6-2 show the recommended CS timing and register configuration to access external RAM and flash.

Register Configurations:
SPI_CS_SETUP = 1; SPI_CS_SETUP_TIME = 0;
SPI_CS_HOLD = 1; SPI_CS_HOLD_TIME = 1.

Figure 26.6-1. Recommended CS Timing and Settings When Accessing External RAM

Register Configurations:
SPI_CS_SETUP = 1; SPI_CS_SETUP_TIME = 0;
SPI_CS_HOLD = 1; SPI_CS_HOLD_TIME = 0.

Figure 26.6-2. Recommended CS Timing and Settings When Accessing Flash
```

```markdown
## 26.7 GP-SPI2 Clock Control

GP-SPI2 has the following clocks:

*   `clk_spi_mst`: module clock of GP-SPI2. When GP-SPI2 works as master, this `clk_spi_mst` is used to generate SPI_CLK signal for data transfer and for slaves.
*   `clk_hclk`: module timing compensation clock of GP-SPI2, which is a frequency-doubled clock derived from the same source as `clk_spi_mst`.
*   `SPI_CLK`: the output clock when the GP-SPI2 works as master.
```