

```markdown
Register 7.28. PCR_I2S_TX_CLKM_DIV_CONF_REG (0x0074)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | (reserved) | PCR_I2S_TX_CLKM_DIV_YN1 | PCR_I2S_TX_CLKM_DIV_X | PCR_I2S_TX_CLKM_DIV_Y | PCR_I2S_TX_CLKM_DIV_Z | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

PCR_I2S_TX_CLKM_DIV_Z   For b <= a/2, the value of I2S_TX_CLKM_DIV_Z is b. For b > a/2, the value of I2S_TX_CLKM_DIV_Z is (a - b). (R/W)

PCR_I2S_TX_CLKM_DIV_Y    For b <= a/2, the value of I2S_TX_CLKM_DIV_Y is (a%b). For b > a/2, the value of I2S_TX_CLKM_DIV_Y is (a%(a - b)). (R/W)

PCR_I2S_TX_CLKM_DIV_X    For b <= a/2, the value of I2S_TX_CLKM_DIV_X is floor(a/b) - 1. For b > a/2, the value of I2S_TX_CLKM_DIV_X is floor(a/(a - b)) - 1. (R/W)

PCR_I2S_TX_CLKM_DIV_YN1  For b <= a/2, the value of I2S_TX_CLKM_DIV_YN1 is 0. For b > a/2, the value of I2S_TX_CLKM_DIV_YN1 is 1. (R/W)
```

Note:
“a” and “b” represent the denominator and the numerator of the fractional divider, respectively. For more information, see Section 31.6 in Chapter I²S Controller (I2S).
```