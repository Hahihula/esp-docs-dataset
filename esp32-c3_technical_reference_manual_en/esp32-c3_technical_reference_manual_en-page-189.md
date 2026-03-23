

```markdown
Register 5.23. GPIO SD SIGMA DELTA n_REG (n: 0-3) (0x0000+4*n)

| 31 | 16 | 15 | ... | 8 | 7 | ... | 0 |
|----|----|----|-----|---|---|-----|---|
| 0  | 0  | 0  | 0   | 0 | 0 | 0   | 0 |

GPIO SD n_IN This field is used to configure the duty cycle of sigma delta modulation output. (R/W)

GPIO SD n_PRESCALE This field is used to set a divider value to divide APB clock. (R/W)


Register 5.24. GPIO SD SIGMA DELTA CG_REG (0x0020)

| 31 | 30 |
|----|----|
| 0  | 0  |

GPIO SD CLK_EN Clock enable bit of configuration registers for sigma delta modulation. (R/W)


Register 5.25. GPIO SD SIGMA DELTA MISC_REG (0x0024)

| 31 | 30 | 29 |
|----|----|----|
| 0  | 0  | 0  |

GPIO SD FUNCTION_CLK_EN Clock enable bit of sigma delta modulation. (R/W)

GPIO SD SPI_SWAP Reserved. (R/W)
```