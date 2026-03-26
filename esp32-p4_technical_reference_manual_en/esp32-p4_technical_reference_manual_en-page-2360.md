

```markdown
- When HP_SYS_CLKRST_I2C1_SRC_SEL is 0, the clock source is XTAL_40M_CLK.
- When HP_SYS_CLKRST_I2C1_SRC_SEL is 1, the clock source is FOSC_20M_CLK.

The steps to configure the clock source for LP_I2C are as follows:

- Enable the clock source for I2C_SCLK of LP_I2C by configuring LPPERI_LCK_EN_LP_I2C to 1.
- When LPPERI_LP_I2C_CLK_SEL is 0, the clock source is LP_DYN_FAST_CLK.
- When LPPERI_LP_I2C_CLK_SEL is 1, the clock source is XTAL_D2_CLK.
- When LPPERI_LP_I2C_CLK_SEL is 2, the clock source is PLL_LP_CLK 8 MHz.

The clock source then passes through a fractional divider to generate I2C_SCLK according to the following equation:

$$
I2C\_SCLK\_DIV\_NUM + 1 + \frac{I2C\_SCLK\_DIV\_A}{I2C\_SCLK\_DIV\_B}
$$

In the equation, I2C_SCLK_DIV_NUM represents the integer part of the divisor, I2C_SCLK_DIV_A represents the numerator of the fractional part of the divisor, and I2C_SCLK_DIV_B represents the denominator of the fractional part of the divisor. Limited by timing parameters, the derived clock I2C_SCLK should operate at a frequency 20 times larger than SCL's frequency.

For I2CO:

- Configure I2C_SCLK_DIV_NUM via HP_SYS_CLKRST_I2CO_CLK_DIV_NUM.
- Configure I2C_SCLK_DIV_A via HP_SYS_CLKRST_I2CO_CLK_DIV_NUMERATOR.
- Configure I2C_SCLK_DIV_B via HP_SYS_CLKRST_I2CO_CLK_DIV_DENOMINATOR.

For I2C1:

- Configure I2C_SCLK_DIV_NUM via HP_SYS_CLKRST_I2C1_CLK_DIV_NUM.
- Configure I2C_SCLK_DIV_A via HP_SYS_CLKRST_I2C1_CLK_DIV_NUMERATOR.
- Configure I2C_SCLK_DIV_B via HP_SYS_CLKRST_I2C1_CLK_DIV_DENOMINATOR.

## 44.4.2 SCL and SDA Noise Filtering

SCL_Filter and SDA_Filter modules are identical and are used to filter signal noise on SCL and SDA, respectively. These filters can be enabled or disabled by configuring I2C_SCL_FILTER_EN and I2C_SDA_FILTER_EN.

Take SCL_Filter as an example. When enabled, SCL_Filter samples input signals on the SCL line continuously. These input signals are valid only if they remain unchanged for consecutive I2C_SCL_FILTER_THRES I2C_SCLK clock cycles. Given that only valid input signals can pass through the filter, SCL_Filter can remove glitches whose pulse width is shorter than I2C_SCL_FILTER_THRES I2C_SCLK clock cycles, while SDA_Filter can remove glitches whose pulse width is shorter than I2C_SDA_FILTER_THRES I2C_SCLK clock cycles.

## 44.4.3 SCL Clock Stretching

The I2C controller in slave mode (i.e., slave) can realize the function called clock stretching by holding the SCL line low to suspend data transmission in exchange for more time to process data. This function is enabled
```