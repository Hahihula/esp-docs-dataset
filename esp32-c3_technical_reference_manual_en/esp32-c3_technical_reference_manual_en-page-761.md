

```markdown
Register 29.18. I2S_TX_CLKM_DIV_CONF_REG (0x003C)

| 31 | 28 | 27 | 26 | 18 | 17 | 9 | 0 |
|----:|----:|----:|----:|----:|----:|---:|---:|
|    | (reserved) | I2S_TX_CLKM_DIV_YN1 | I2S_TX_CLKM_DIV_X | I2S_TX_CLKM_DIV_Y | I2S_TX_CLKM_DIV_Z |
| 0 | 0 | 0 | 0 | 0x0 | 0x1 | 0x0 | Reset |

I2S_TX_CLKM_DIV_Z   For b <= a/2, the value of I2S_TX_CLKM_DIV_Z is b. For b > a/2, the value of I2S_TX_CLKM_DIV_Z is (a - b). (R/W)

I2S_TX_CLKM_DIV_Y    For b <= a/2, the value of I2S_TX_CLKM_DIV_Y is (a%b). For b > a/2, the value of I2S_TX_CLKM_DIV_Y is (a%(a - b)). (R/W)

I2S_TX_CLKM_DIV_X    For b <= a/2, the value of I2S_TX_CLKM_DIV_X is floor(a/b) - 1. For b > a/2, the value of I2S_TX_CLKM_DIV_X is floor(a/(a - b)) - 1. (R/W)

I2S_TX_CLKM_DIV_YN1  For b <= a/2, the value of I2S_TX_CLKM_DIV_YN1 is 0. For b > a/2, the value of I2S_TX_CLKM_DIV_YN1 is 1. (R/W)


Note:
"a" and "b" represent the denominator and the numerator of fractional divider, respectively. For more information, see Section 29.6.
```