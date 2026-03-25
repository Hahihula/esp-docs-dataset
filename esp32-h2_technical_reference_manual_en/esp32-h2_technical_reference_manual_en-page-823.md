

```markdown
## Register 29.12. SPI_CLOCK_REG (0x000C)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | reserved          |                                                                             |
| 30  | reserved          |                                                                             |
| 29  | reserved          |                                                                             |
| 28  | SPI_CLKDIV_PRE    | Configures the pre-divider of SPI_CLK in master transfer. Can be configured in CONF state. (R/W) |
| 27  | SPI_CLK_EQU_SYSCLK| Configures whether or not the SPI_CLK is equal to APB_CLK in master transfer.<br>0: SPI_CLK is divided from APB_CLK.<br>1: SPI_CLK is equal to APB_CLK.<br>Can be configured in CONF state. (R/W) |
| 26  | reserved          |                                                                             |
| 25  | SPI_CLK_EDGE_SEL  | Configures whether to use the standard clock sampling edge or delay the sampling edge by half a cycle during master transfer.<br>0: The clock sampling edge is delayed by half a cycle.<br>1: The clock sampling edge is standard.<br>Can be configured in CONF state. (R/W) |
| 24  | reserved          |                                                                             |
| 23  | SPI_CLKCNT_N      | Configures the divider of SPI_CLK in master transfer.<br>SPI_CLK frequency = f_clk_spi_mst/(SPI_CLKDIV_PRE + 1)/(SPI_CLKCNT_N + 1).<br>Can be configured in CONF state. (R/W) |
| 22  | reserved          |                                                                             |
| 21  | SPI_CLKCNT_H      | Configures the duty cycle of SPI_CLK (high level) in master transfer.<br>It's recommended to configure this value to floor((SPI_CLKCNT_N + 1)/2 - 1).<br>floor() here is to round a number down, e.g., floor(2.2) = 2.<br>In slave mode, it must be 0.<br>Can be configured in CONF state. (R/W) |
| 20  | reserved          |                                                                             |
| 19  | SPI_CLKCNT_L      | In master transfer, this field must be equal to SPI_CLKCNT_N.<br>In slave mode, it must be 0.<br>Can be configured in CONF state. (R/W) |
| 18  | reserved          |                                                                             |
| 17  | reserved          |                                                                             |
| 16  | reserved          |                                                                             |
| 15  | SPI_CLKCNT_N      |                                                                             |
| 14  | SPI_CLKCNT_H      |                                                                             |
| 13  | SPI_CLKCNT_L      |                                                                             |
| 12  | reserved          |                                                                             |
| 11  | reserved          |                                                                             |
| 10  | reserved          |                                                                             |
| 9   | reserved          |                                                                             |
| 8   | reserved          |                                                                             |
| 7   | reserved          |                                                                             |
| 6   | reserved          |                                                                             |
| 5   | reserved          |                                                                             |
| 4   | reserved          |                                                                             |
| 3   | reserved          |                                                                             |
| 2   | reserved          |                                                                             |
| 1   | reserved          |                                                                             |
| 0   | Reset             | 0x3                                                                              |

## Register 29.13. SPI_CLK_GATE_REG (0x00E8)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | reserved          |                                                                             |
| 30  | reserved          |                                                                             |
| 29  | reserved          |                                                                             |
| ... | ...                | ...                                                                           |
| 4   | reserved          |                                                                             |
| 3   | SPI_CLK_EN        | Configures whether or not to enable clock gate.<br>0: Disable<br>1: Enable<br>(R/W) |
| 2   | reserved          |                                                                             |
| 1   | reserved          |                                                                             |
| 0   | Reset             | 0                                                                              |
```