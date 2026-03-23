

```markdown
Chapter 29 I2S Controller (I2S)

The following formula shows the relation between I2S_TX/RX_CLK frequency /f_I2S_TX/RX_CLK/ and the divider clock source frequency f_I2S_CLK_S:

    f_I2S_TX/RX_CLK = (f_I2S_CLK_S) / (N + b/a)

N is an integer value between 2 and 256. The value of N corresponds to the value of I2S_TX/RX_CLKM_DIV_NUM in register I2S_TX/RX_CLKM_CONF_REG as follows:

* When I2S_TX/RX_CLKM_DIV_NUM = 0, N = 256.
* When I2S_TX/RX_CLKM_DIV_NUM = 1, N = 2.
* When I2S_TX/RX_CLKM_DIV_NUM has any other value, N = I2S_TX/RX_CLKM_DIV_NUM.

The values of “a” and “b” in fractional divider depend only on x, y, z, and yn1. The corresponding formulas are as follows:

* When b <= a/2 , yn1 = 0, x = floor([a/b]) - 1, y = a%b, z = b;
* When b > a/2 , yn1 = 1, x = floor([a-b]/b) - 1, y = a%(a - b), z = a - b.

The values of x, y, z, and yn1 are configured in I2S_TX/RX_CLKM_DIV_X, I2S_TX/RX_CLKM_DIV_Y, I2S_TX/RX_CLKM_DIV_Z, and I2S_TX/RXCLKM_DIV_YN1. To configure the integer divider, clear I2S_TX/RX_CLKM_DIV_X and I2S_TX/RX_CLKM_DIV_Z, then set I2S_TX/RX_CLKM_DIV_Y to 1.

Note:
Using fractional divider may introduce some clock jitter.

In master TX mode, the serial clock BCK for I2S_TX unit is I2SO_BCK_out, divided from I2S_TX_CLK. That is:

    f_I2SO_BCK_out = (f_I2S_TX_CLK) / MO

“MO” is an integer value:

    MO = I2S_TX_BCK_DIV_NUM + 1

Note:
I2S_TX_BCK_DIV_NUM must not be configured as 1.

In master RX mode, the serial clock BCK for I2S_RX unit is I2SI_BCK_out, divided from I2S_RX_CLK. That is:

    f_I2SI_BCK_out = (f_I2S_RX_CLK) / MI

“MI” is an integer value:

    MI = I2S_RX_BCK_DIV_NUM + 1
```