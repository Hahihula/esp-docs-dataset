

```markdown
Register 28.11. SPI_SLAVE1_REG (0x00E4)

| 31 | 26 | 25 | 18 | 17 | 0 |
|----:|----:|----:|----:|----:|---|
|   O |   O |   O |   O |   O |Reset|

SPI_SLV_DATA_BITLEN Configures the transferred data bit length in SPI slave full-/half-duplex modes. (R/W/SS)

SPI_SLV_LAST_COMMAND Configures the command value in slave mode. (R/W/SS)

SPI_SLV_LAST_ADDR Configures the address value in slave mode. (R/W/SS)


Register 28.12. SPI_CLOCK_REG (0x000C)

| 31 | 30 | 22 | 21 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|---:|---:|---|
|   1 |   O |   O |   O |   O |   O |   O |   O |   O |   O |Reset|

SPI_CLKCNT_L In master transfer, this field must be equal to SPI_CLKCNT_N. In slave mode, it must be 0. Can be configured in CONF state. (R/W)

SPI_CLKCNT_H Configures the duty cycle of SPI_CLK (high level) in master transfer. (R/W)
It's recommended to configure this value to floor((SPI_CLKCNT_N + 1)/2 - 1). floor() here is to round a number down, e.g., floor(2.2) = 2. In slave mode, it must be 0.
Can be configured in CONF state.

SPI_CLKCNT_N Configures the divider of SPI_CLK in master transfer. (R/W)
SPI_CLK frequency is f_clk_spi_mst/(SPI_CLKDIV_PRE + 1)/(SPI_CLKCNT_N + 1).
Can be configured in CONF state.

SPI_CLKDIV_PRE Configures the pre-divider of SPI_CLK in master transfer. (R/W)
Can be configured in CONF state.

SPI_CLK_EQU_SYSCLK Configures whether or not the SPI_CLK is equal to clk_spi_mst in master transfer. (R/W)

* 0: SPI_CLK is divided from clk_spi_mst.
* 1: SPI_CLK is equal to clk_spi_mst.

Can be configured in CONF state.
```