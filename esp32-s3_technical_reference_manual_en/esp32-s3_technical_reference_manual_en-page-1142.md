**Title: Chapter 30 SPI Controller (SPI)**

---

### Figure Caption:
Figure 30-62. Recommended CS Timing and Settings When Accessing Flash

---

#### Section Title:
30.7 GP-SPI Clock Control

---

GP-SPI has the following clocks:

- **clk_spi_mst:** module clock of GP-SPI, derived from PLL_CLK or XTAL_CLK. It is controlled by bits SPI_MST.
  - `_CLK_ACTIVE` and `SPI_MST_CLK_SEL`. Used in GP-SPI master mode to generate `SPI_CLK` signal for data transfer and for slaves.

- **clk_hclk:** module timing compensation clock of GP-SPI. When PLL_CLK is available and the bit `SPI_TIMING` is set, the frequency is 160 MHz; otherwise it's powered off.
  
- **SPI_CLK:** output clock in master mode.

- **APB_CLK:** clock for register configuration.

In master mode, the maximum output clock frequency of GP-SPI is \( f_{clk_spi_mst} \). To have slower frequencies, the output clock frequency can be divided as follows:
\[ f_{SPI_CLK} = \frac{f_{clk_spi_mst}}{(SPI_CLKCNT_N + 1)(SPI_CLKDIV_PRE + 1)} \]

The divider is configured by `SPI_CLKCNT_N` and `SPI_CLKDIV_PRE` in register `SPI_CLOCK_REG`. When the bit `SPI_CLK_EQU_SYSCLK` in register `SPI_CLOCK_REG` is set to 1, the output clock frequency of GP-SPI will be \( f_{clk_spi_mst} \). And for other integral clock divisions, `SPI_CLK_EQU_SYSCLK` should be set to 0.

In slave mode, the supported input clock frequency (\( f_{SPI_CLK} \)) of GP-SPI is:
- If \( f_{APB_CLK} \geq 60 MHz \), \( f_{SPI_CLK} \leq 60 MHz \);
- If \( f_{APB_CLK} < 60 MHz \), \( f_{SPI_CLK} \leq f_{APB_CLK} \).

---

**Footer:**
Espressif Systems  
1142 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback