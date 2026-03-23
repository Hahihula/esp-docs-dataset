

```markdown
Register 8.11. PCR_RMT_SCLK_CONF_REG (0x0030)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 23  | PCR_RMT_SCLK_EN                | Configures whether or not to enable RMT function clock. <br> 0: Not enable <br> 1: Enable (R/W) |
| 22  | PCR_RMT_SCLK_SEL               | Configures to select clock source. <br> 0: Not select any clock <br> 1 (default): Select PLL_F80M_CLK <br> 2: Select RC_FAST_CLK <br> 3: Select XTAL_CLK (R/W) |
| 21  | PCR_RMT_SCLK_DIV_A             | Configures the denominator of the frequency divider factor for RMT function clock. (R/W) |
| 20  | PCR_RMT_SCLK_DIV_B             | Configures the numerator of the frequency divider factor for RMT function clock. (R/W) |
| 19  | PCR_RMT_SCLK_DIV_NUM           | Configures the integral part of the frequency divider factor for RMT function clock. (R/W) |
| 12  | PCR_RMT_SCLK_DIV_B             |                                                                             |
| 11  | PCR_RMT_SCLK_DIV_A             |                                                                             |
| 6   | PCR_RMT_SCLK_DIV_B             |                                                                             |
| 5   | PCR_RMT_SCLK_DIV_NUM           |                                                                             |
| 0   | Reset                          |                                                                             |
```