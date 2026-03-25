

```markdown
Chapter 29 SPI Controller (SPI)

GoBack

* clk_spi_mst: module clock of GP-SPI2, derived from PLL_CLK. Used in GP-SPI2 as master to generate SPI_CLK signal for data transfer and for slaves.
* SPI_CLK: output clock as master.
* APB_CLK: clock for register configuration.

clk_spi_mst is enabled by PCR_SPI2_MST_CLK_ACTIVE_I and its clock source is controlled by PCR_SPI2_MST_CLK_SEL_I[1:0]:

  * 0: XTAL_CLK
  * 1: PLL_F48M_CLK
  * 2: RC_FAST_CLK

When operating as master, the maximum output clock frequency of GP-SPI2 is f_clk_spi_mst. To have slower frequencies, the output clock frequency can be divided as follows:

$$f_{SPI\_CLK} = \frac{f_{clk\_spi\_mst}}{(SPI\_CLKCNT\_N + 1)(SPI\_CLKDIV\_PRE + 1)}$$

The divider is configured by SPI_CLKCNT_N and SPI_CLKDIV_PRE in register SPI_CLOCK_REG. When the bit SPI_CLK_EQU_SYSCLK in register SPI_CLOCK_REG is set to 1, the output clock frequency of GP-SPI2 will be f_clk_spi_mst. For other integral clock divisions, SPI_CLK_EQU_SYSCLK should be set to 0.

When operating as slave, the input clock frequency supported by GP-SPI2 is f_clk_spi_slv, and

* If f_AHB_CLK >= 40 MHz, f_clk_spi_slv <= 40 MHz;
* If f_AHB_CLK < 40 MHz, f_clk_spi_slv <= f_AHB_CLK.

29.71 Clock Phase and Polarity

SPI protocol has four clock modes, i.e., modes 0 ~ 3. See Figure 29.7-1 and Figure 29.7-2 (excerpted from SPI protocol).

Note:
The images are sourced from the SPI protocol. In the two images, the black **SAMPLE** signal represents the standard sampling edge, while the red represents the default sampling edge of GP-SPI.
```