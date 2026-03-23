

```markdown
Figure 27.6-2. Recommended CS Timing and Settings When Accessing Flash

Register Configurations:

SPI_CS_SETUP = 1; SPI_CS_SETUP_TIME = 0;
SPI_CS_HOLD = 1; SPI_CS_HOLD_TIME = 0.

## 27.7 GP-SPI2 Clock Control

GP-SPI2 has the following clocks:

*   clk_spi_mst: module clock of GP-SPI2, derived from PLL_CLK. Used in GP-SPI2 master mode, to generate SPI_CLK signal for data transfer and for slaves.
*   SPI_CLK: output clock in master mode.
*   APB_CLK: clock for register configuration.
*   clk_hclk: module timing compensation clock of GP-SPI2.

In master mode, the maximum output clock frequency of GP-SPI2 is $f_{\text{clk\_spi\_mst}}$. To have slower frequencies, the output clock frequency can be divided as follows:

$$
f_{\text{SPI_CLK}} = \frac{f_{\text{clk\_spi\_mst}}}{(\text{SPI_CLKCNT}_N + 1)(\text{SPI_CLKDIV\_PRE} + 1)}
$$

The divider is configured by SPI_CLKCNT_N and SPI_CLKDIV_PRE in register SPI_CLOCK_REG. When the bit SPI_CLK_EQU_SYSCLK in register SPI_CLOCK_REG is set to 1, the output clock frequency of GP-SPI2 will be $f_{\text{clk\_spi\_mst}}$. And for other integral clock divisions, SPI_CLK_EQU_SYSCLK should be set to 0.

In slave mode, the supported input clock frequency ($f_{\text{SPI_CLK}}$) of GP-SPI2 is:

*   If $f_{\text{APB_CLK}} >= 60 \text{ MHz}$, $f_{\text{SPI_CLK}} <= 60 \text{ MHz}$;
*   If $f_{\text{APB_CLK}} < 60 \text{ MHz}$, $f_{\text{SPI_CLK}} <= f_{\text{APB_CLK}}$.

## 27.7.1 Clock Phase and Polarity

There are four clock modes in SPI protocol, modes 0 ~ 3, see Figure 27.7-1 and Figure 27.7-2 (excerpted from SPI protocol):
```