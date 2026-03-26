

```markdown
## Register 10.4. HP_SYS_CLKRST_ROOT_CLK_CTRL2_REG (0x000C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-24     | `HP_SYS_CLKRST_APB_CLK_DIV_NUMERATOR`      | Configures the numerator of the divisor's fractional part for SYS_CLK. (R/W) |
| 23-16     | `HP_SYS_CLKRST_APB_CLK_DIV_DENOMINATOR`    | Configures the denominator of the divisor's fractional part for SYS_CLK. (R/W)|
| 15-8      | `HP_SYS_CLKRST_APB_CLK_DIV_NUM`            | Configures the integer part of the APB_CLK fclock divisor. (R/W)             |
| 7-0       | `HP_SYS_CLKRST_APB_CLK_DIV_NUMERATOR`      | Configures the numerator of the divisor's fractional part for APB_CLK. (R/W)|

## Register 10.5. HP_SYS_CLKRST_ROOT_CLK_CTRL3_REG (0x0010)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-8      | `reserved`                                 | RESERVED                                                                     |
| 7-0       | `HP_SYS_CLKRST_APB_CLK_DIV_DENOMINATOR`    | Configures the denominator of the divisor's fractional part for APB_CLK. (R/W)|
```