

```markdown
- 48 MHz XTAL_CLK
- 240 MHz PLL_F240M_CLK
- 160 MHz PLL_F160M_CLK
- I2S_MCLK_in (external input clock)

The serial clock (BCK) of the I2S TX/RX unit is divided from I2S_TX/RX_CLK, as shown in Figure 35.6-1.
PCR_I2S_TX/RX_CLKM_SEL is used to select clock source for TX/RX unit, and PCR_I2S_TX/RX_CLKM_EN to
enable or disable the clock source.

![Figure 35.6-1. I2S Clock Generator](image_path)

The following formula shows the relation between I2S_TX/RX_CLK frequency fI2S_TX/RX_CLK and the divider
clock source frequency fI2S_CLK_S:

fI2S_TX/RX_CLK = (fI2S_CLK_S) / (N + b/a)

N is an integer value between 2 and 256. The value of N is mapped to that of PCR_I2S_TX/RX_CLKM_DIV_NUM as follows:
- When PCR_I2S_TX/RX_CLKM_DIV_NUM = 0, N = 256;
- When PCR_I2S_TX/RX_CLKM_DIV_NUM = 1, N = 2;
- When PCR_I2S_TX/RX_CLKM_DIV_NUM has any other value, N = PCR_I2S_TX/RX_CLKM_DIV_NUM.

The values of “a” and “b” in fractional divider depend only on x, y, z, and yn1. The corresponding formulas are
as follows:
- When b <= a/2, yn1 = 0, x = floor((a/b) - 1), y = a%b, z = b;
- When b > a/2, yn1 = 1, x = floor((a/a-b) - 1), y = a%(a - b), z = a - b.

The values of x, y, z, and yn1 are configured in PCR_I2S_TX/RX_CLKM_DIV_X, PCR_I2S_TX/RX_CLKM_DIV_Y,
PCR_I2S_TX/RX_CLKM_DIV_Z, and PCR_I2S_TX/RX_CLKM_DIV_YN1.
```