

```markdown
| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                 |                                                                             |
| 23  | PCR_UART1_SCLK_DIV_A       | Configures the denominator of the frequency divider factor for UART1 function clock. (R/W) |
| 22  |                             |                                                                             |
| 21  | PCR_UART1_SCLK_DIV_B       | Configures the numerator of the frequency divider factor for UART1 function clock. (R/W) |
| 20  |                             |                                                                             |
| 19  | PCR_UART1_SCLK_SEL         | Configures to select clock source.<br>0: Not select any clock<br>1: Select PLL_F80M_CLK<br>2: Select RC_FAST_CLK<br>3: Select XTAL_CLK (R/W) |
| 18  |                             |                                                                             |
| 17  | PCR_UART1_SCLK_EN          | Configures whether or not to enable UART1 function clock.<br>0: Not enable<br>1: Enable (R/W) |
| 16  |                             |                                                                             |
| 15  |                             |                                                                             |
| 14  |                             |                                                                             |
| 13  | PCR_UART1_SCLK_DIV_NUM     | Configures the integral part of the frequency divider factor for UART1 function clock. (R/W) |
| 12  |                             |                                                                             |
| 11  |                             |                                                                             |
| 10  |                             |                                                                             |
| 9   |                             |                                                                             |
| 8   |                             |                                                                             |
| 7   |                             |                                                                             |
| 6   | PCR_UART1_SCLK_DIV_B       |                                                                             |
| 5   |                             |                                                                             |
| 4   |                             |                                                                             |
| 3   |                             |                                                                             |
| 2   |                             |                                                                             |
| 1   |                             |                                                                             |
| 0   | Reset                      |                                                                             |
```