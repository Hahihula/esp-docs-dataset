

```markdown
Chapter 46 I2S Controller (I2S)

The following formula shows the relation between I2Sn_TX/RX_CLK frequency fI2Sn_TX/RX_CLK and the divider clock source frequency fI2Sn_CLK_S:

fI2Sn_TX/RX_CLK = fI2Sn_CLK_S / (N + b/a)

N is an integer value between 2 and 256. The value of N is mapped to that of HP_SYS_CLKRST_I2Sn_TX/RX_DIV_N as follows:
* When HP_SYS_CLKRST_I2Sn_TX/RX_DIV_N = 0, N = 256;
* When HP_SYS_CLKRST_I2Sn_TX/RX_DIV_N = 1, N = 2;
* When HP_SYS_CLKRST_I2Sn_TX/RX_DIV_N has any other value, N = HP_SYS_CLKRST_I2Sn_TX/RX_DIV_N.

The values of “a” and “b” in fractional divider depend only on x, y, z, and yn1. The corresponding formulas are as follows:
* When b <= a/2, yn1 = 0, x = floor((a-1)/5) - 1, y = a%b, z = b;
* When b > a/2, yn1 = 1, x = floor(((a-b)/5)) - 1, y = a%(a-b), z = a - b.

The values of x, y, z, and yn1 are configured in HP_SYS_CLKRST_I2Sn_TX/RX_DIV_X, HP_SYS_CLKRST_I2Sn_TX/RX_DIV_Y, HP_SYS_CLKRST_I2Sn_TX/RX_DIV_Z, and HP_SYS_CLKRST_I2Sn_TX/RX_DIV_YN1.

To configure the integer divider, clear HP_SYS_CLKRST_I2Sn_TX/RX_DIV_X and HP_SYS_CLKRST_I2Sn_TX/RX_DIV_Z, then set HP_SYS_CLKRST_I2Sn_TX/RX_DIV_Y to 1.

Note:
Using fractional divider may introduce some clock jitter.

In master TX mode, the serial clock BCK for I2Sn TX unit is I2SnO_BCK_out divided from I2Sn_TX_CLK which is:

fI2SnO_BCK_out = fI2Sn_TX_CLK / MO

“MO” is an integer value:

MO = I2Sn_TX_BCK_DIV_NUM + 1

Note:
Note that I2S_TX_BCK_DIV_NUM must not be configured as 1.

In master RX mode, the serial clock BCK for I2Sn RX unit is I2SnI_BCK_out divided from I2Sn_RX_CLK, which is:

fI2SnI_BCK_out = fI2Sn_RX_CLK / MI

“MI” is an integer value:

MI = I2S_RX_BCK_DIV_NUM + 1
```