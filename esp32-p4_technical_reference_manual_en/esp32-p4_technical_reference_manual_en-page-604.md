

```markdown
## 9.20.3 GPIO EXT Registers

The addresses in this section are relative to (HP GPIO matrix base address + 0xOF00). GPIO base address is provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX .

### Register 9.45. GPIO_EXT_SIGMADELTA_REG (n: 0 - 7) (0x0000+0x4*n)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        |                                | (reserved)                                                                  |
| 16        | GPIO_EXT_SDn_PRESCALE          | Configures the divider value to divide HP IO MUX operating clock. Can be 0 ~ 255.<br>0: Do not divide<br>1 ~ 255: The clock is divided by 2 ~ 256 (R/W) |
| 8         | GPIO_EXT_SDn_IN                | Configures the duty cycle of sigma delta modulation output. (R/W)            |
| 7-0       |                                | (reserved)                                                                  |

### Register 9.46. GPIO_EXT_SIGMADELTA_MISC_REG (0x0024)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        |                                | (reserved)                                                                  |
| 30        | GPIO_EXT_SD_FUNCTION_CLK_EN    | Configures whether or not to enable the clock for sigma delta modulation.<br>0: Not enable<br>1: Enable (R/W) |
```