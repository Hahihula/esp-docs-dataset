

```markdown
f_SPI_CLK = f_clk_spi_mst / (SPI_CLKCNT_N + 1) * (SPI_CLKDIV_PRE + 1)

The divider is configured by SPI_CLKCNT_N and SPI_CLKDIV_PRE in register SPI_CLOCK_REG. When the bit SPI_CLK_EQU_SYSCLK in register SPI_CLOCK_REG is set, the output clock frequency of GP-SPI will be f_clk_spi_mst. For other integral clock divisions, SPI_CLK_EQU_SYSCLK should be cleared.

When operating as slave, the supported input clock frequency (f_SPI_CLK) of GP-SPI is:

* If f_AHB_CLK >= 60 MHz, f_SPI_CLK <= 60 MHz.
* If f_AHB_CLK < 60 MHz, f_SPI_CLK <= f_AHB_CLK.

## 43.7.2 LP-SPI Clock Control

LP-SPI has the following clocks:

* lp_spi_pclk: LP-SPI module clock and clock for register configuration. lp_spi_pclk is used to generate LP_SPI_CLK for data transfer and for slaves when LP-SPI works as master. LPPERI_CK_EN_LP_SPI is used to enable this lp_spi_pclk.
* LP_SPI_CLK: output clock as master.

## 43.7.3 Clock Phase and Polarity

SPI protocol has four clock modes, i.e., modes 0~3. See Figure 43.7-1 and Figure 43.7-2 (excerpted from SPI protocol):

![Figure 43.7-1. SPI Clock Mode 0 or 2](image)

MSB first (LSBF = 0): MSB Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | LSB
LSB first (LSBF = 1): LSB Bit 1 | Bit 2 | Bit 3 | Bit 4 | Bit 5 | Bit 6 | MSB

t_L = Minimum leading time before the first SCK edge
t_T = Minimum trailing time after the last SCK edge
t_I = Minimum idling time between transfers (minimum SS high time)
t_L, t_T and t_I are guaranteed for the master mode and required for the slave mode.
```