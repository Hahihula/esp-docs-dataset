

```markdown
- Up to 40 MHz LP_FAST_CLK with configurable clock source
- 20 MHz XTAL_D2_CLK
- 8 MHz PLL_LP_CLK

The serial clock (BCK) of the LP I2S RX unit is divided from LP_I2S_RX_CLK, as shown in Figure 47.5-1.
LPPERI_LP_I2S_RX_CLK_SEL is used to select clock source for the LP I2S RX unit, and
LPPERI_CLK_EN_LP_I2S_RX to enable or disable the clock source.

![Figure 47.5-1. LP I2S Clock Generator](image_path_if_available)

The following formula shows the relation between LP_I2S_RX_CLK frequency f_LP_I2S_RX_CLK and the divider
clock source frequency f_LP_I2S_CLK_S:

f_LP_I2S_RX_CLK = (f_LP_I2S_CLK_S) / (N + b/a)

N is an integer value between 2 and 256. The value of N is mapped to that of LPPERI_LP_I2S_RX_CLKM_DIV_N as follows:
- When LPPERI_LP_I2S_RX_CLKM_DIV_N = 0, N = 256;
- When LPPERI_LP_I2S_RX_CLKM_DIV_N = 1, N = 2;
- When LPPERI_LP_I2S_RX_CLKM_DIV_N has any other value, N = LPPERI_LP_I2S_RX_CLKM_DIV_NUM.

The values of “a” and “b” in fractional divider depend only on x, y, z, yn1. The corresponding formulas are
as follows:

- When b <= a/2, yn1 = 0, x = floor((a/b) - 1), y = a%b, z = b;
- When b > a/2, yn1 = 1, x = floor(([a-b]/5)) - 1, y = a%(a-b), z = a - b.

The values of x, y, z, and yn1 are configured by LPPERI_LP_I2S_RX_CLKM_DIV_X,
LPPERI_LP_I2S_RX_CLKM_DIV_Y, LPPERI_LP_I2S_RX_CLKM_DIV_Z and
LPPERI_LP_I2S_RX_CLKM_DIV_YN1.

To configure the integer divider, clear LPPERI_LP_I2S_RX_CLKM_DIV_X and LPPERI_LP_I2S_RX_CLKM_DIV_Z,
then set LPPERI_LP_I2S_RX_CLKM_DIV_Y to 1.

Note:
Using fractional divider may introduce some clock jitter.
```
In master RX mode, the serial clock BCK for LP I2S RX unit is LP_I2SI_BCK_out divided from LP_I2S_RX_CLK,
which is:
```