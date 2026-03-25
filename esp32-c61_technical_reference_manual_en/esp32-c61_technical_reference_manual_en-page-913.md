

```markdown
- AHB_CLK: clock for register configuration.

clk_spi_mst is enabled by PCR_SPI2_CLK_EN and its clock source is controlled by
PCR_SPI2_CLKMST_SEL:

• 0: XTAL_CLK
• 1: PLL_F160M_CLK
• 2: FOSC_CLK

When operating as master, the maximum output clock frequency of GP-SPI2 is $f_{clk\_spi\_mst}$. To have slower frequencies, the output clock frequency can be divided as follows:

$$f_{SPI\_CLK} = \frac{f_{clk\_spi\_mst}}{(SPI\_CLKCNT\_N + 1)(SPI\_CLKDIV\_PRE + 1)}$$

The divider is configured by SPI_CLKCNT_N and SPI_CLKDIV_PRE in register SPI_CLOCK_REG. When the bit SPI_CLK_EQU_SYSCLK in register SPI_CLOCK_REG is set, the output clock frequency of GP-SPI2 will be $f_{clk\_spi\_mst}$. For other integral clock divisions, SPI_CLK_EQU_SYSCLK should be cleared.

When operating as slave, the supported input clock frequency ($f_{SPI\_CLK}$) of GP-SPI2 is $f_{SPI\_CLK} <= f_{AHB\_CLK}$.
```

## 26.7.1 Clock Phase and Polarity

SPI protocol has four clock modes, i.e., modes 0~3. See Figure 26.7-1 and Figure 26.7-2.

**Note:**
The images are sourced from the SPI protocol. In the two images, the black SAMPLE signal represents the standard sampling edge, while the red represents the default sampling edge of GP-SPI2.
```