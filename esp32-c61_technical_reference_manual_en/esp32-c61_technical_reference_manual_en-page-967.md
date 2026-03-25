

```markdown
Chapter 27 I2C Controller (I2C)

You can configure the clock source for I2C_SCLK of I2C in the main system to XTAL_CLK or RC_FAST_CLK via PCR_I2C_SCLK_SEL.

The steps to configure the clock source for I2C are as follows:

* Enable the clock source for I2C_SCLK of I2C by configuring `PCR_I2C_SCLK_EN` to 1.
* When `PCR_I2C_SCLK_SEL` is 0, the clock source is XTAL_CLK.
* When `PCR_I2C_SCLK_SEL` is 1, the clock source is RC_FAST_CLK.

The clock source then passes through a fractional divider to generate I2C_SCLK of I2C according to the following formula:

```
I2C_SCLK_DIV_NUM + 1 + (I2C_SCLK_DIV_A / I2C_SCLK_DIV_B)
```

In the formula, `I2C_SCLK_DIV_NUM` represents the integer part of the divisor, `I2C_SCLK_DIV_A` represents the numerator of the fractional part of the divisor, and `I2C_SCLK_DIV_B` represents the denominator of the fractional part of the divisor. Limited by timing parameters, the derived clock I2C_SCLK should operate at a frequency 20 times larger than SCL's frequency.

For I2C:

* Configure `I2C_SCLK_DIV_NUM` via `PCR_I2C_SCLK_DIV_NUM`.
* Configure `I2C_SCLK_DIV_A` via `PCR_I2C_SCLK_DIV_A`.
* Configure `I2C_SCLK_DIV_B` via `PCR_I2C_SCLK_DIV_B`.

## 27.4.2 SCL and SDA Noise Filtering

SCL_Filter and SDA_Filter modules are identical and are used to filter signal noise on SCL and SDA, respectively. These filters can be enabled or disabled by configuring `I2C_SCL_FILTER_EN` and `I2C_SDA_FILTER_EN`.

Take SCL_Filter as an example. When enabled, SCL_Filter samples input signals on the SCL line continuously. These input signals are valid only if they remain unchanged for consecutive `I2C_SCL_FILTER_THRES` I2C_SCLK clock cycles. Given that only valid input signals can pass through the filter, SCL_Filter can remove glitches whose pulse width is shorter than `I2C_SCL_FILTER_THRES` I2C_SCLK clock cycles, while SDA_Filter can remove glitches whose pulse width is shorter than `I2C_SDA_FILTER_THRES` I2C_SCLK clock cycles.

## 27.4.3 SCL Clock Stretching

The I2C controller operating in slave mode (i.e., as a slave) can perform clock stretching by holding the SCL line low. This action suspends data transmission, providing more time to process data. This function is enabled by setting the `I2C_SLAVE_SCL_STRETCH_EN` bit. The time period for releasing the SCL line from stretching is configured by setting the `I2C_STRETCH_PROTECT_NUM` field to avoid timing sequence errors.

The slave can activate clock stretching by pulling the SCL line low in response to one of four specific events.
```