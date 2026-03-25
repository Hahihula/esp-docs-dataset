

```markdown
Chapter 8 GPIO Matrix and IO MUX

Register 8.28. GPIO_EXT_SIGMADELTA{n}_REG (n: 0-3) (0x0008+0x4*n)

| 31 | 16 | 15 | ... | 8 | 7 | ... | 0 |
|----|----|----|-----|---|---|-----|---|
| 0  | 0  | 0  | ... | 0 | 0 | ... | 0 |
|    |    |    |     |   |   |     | Reset |

GPIO_EXT_SD{n}_IN Configures the duty cycle of sigma delta modulation output.
(R/W)

GPIO_EXT_SD{n}_PRESCALE Configures the divider value to divide IO MUX operating clock.

0: Do not divide
1~255: The clock is divided by 2~256

(R/W)
```