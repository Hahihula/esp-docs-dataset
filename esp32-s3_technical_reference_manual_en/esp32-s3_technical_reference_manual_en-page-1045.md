**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Navigation Link:**
GoBack

**List of Clock Sources and Their Frequencies:**
- 40 MHz XTAL_CLK
- 160 MHz PLL_F160M_CLK
- 240 MHz PLL_D2_CLK
- or external input clock: I2Sn_MCLK_in

**Description with Formula Explanation for Clock Source Selection (I2S_TX/RX_CLK_SEL):**
I2S_TX/RX_CLK_SEL is used to select the clock source for TX/RX unit, and I2S_TX/RX_CLK_ACTIVE to enable or disable the clock source.

**Figure Description:**
- Figure 28.6-1 illustrates an "I2Sn Clock" with various components like XTAL_CLK, PLL_D2_CLK, and I2S_MCLK_IN.
- The diagram shows a block labeled “I2Sn_TX_CLKSEL[0]” connected to different clock sources.

**Explanation of Formula:**
The following formulae show the relation between "I2Sn_TX/RX_CLK" frequency (f12Sn_TX/RX_CLK) and the divider clock source frequency f12Sn_CLK_s:
\[ f_{\text{I2S}_{n}\_\text{TX}/\text{RX}_{Clk}} = \frac{f_{\text{I2S}_{n}\_\text{CLK}_s}}{\frac{N}{b} + a} \]

**Explanation of Integer N:**
- \( N \) is an integer value between 2 and 256.
- The corresponding values for I2S_TX/RX_CLK_DIV_NUM in register I2S_TX/RX_CLKM_CONF_REG are:
  - When `I2S_TX/RX_CLKM_DIV_NUM = 0`, then \( N = 256 \).
  - When `I2S_TX/RX_CLKM_DIV_NUM = 1`, then \( N = 2 \).
  - For any other value of I2S_TX/RX_CLKM_DIV_NUM, the corresponding formula is:
    \[ f_{\text{I2S}_{n}\_\text{TX}/\text{RX}_{Clk}} = \frac{f_{\text{I2S}_{n}\_\text{CLK}_s}}{\frac{N}{b} + a} \]

**Explanation of Fractional Dividers:**
- The values for "a" and "b" in the fractional divider depend on x, y, z, and yn1. Corresponding formulas are:
  - When \( b = \frac{a}{2} \), then \( y = \text{floor}\left(\frac{\text{[x]}}{2}\right) \).
  - For other values of "b", the formula is similar but adjusted based on specific conditions.

**Configuration Values:**
- The configuration for x, y, z, and yn1 are set in I2S_TX/RX_CLKM_DIV_X, I2S_TX/RX_CLKM_DIV_Y, I2S_TX/RX_CLK, M_DIV_Z, and I2S_TX/RXCLKM_DIVYN1.

**Footer:**
- Page number 1045
- Document title ESP32-S3 TRM (Version 1.7)
- Submission Feedback link

This document appears to be a technical manual or guide for configuring the clock settings in an Integrated Circuit, specifically related to I2S Controller configuration on the ESP32-S3 chip by Espressif Systems.