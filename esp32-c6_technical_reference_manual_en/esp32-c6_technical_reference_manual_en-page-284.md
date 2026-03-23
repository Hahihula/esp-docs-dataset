

```markdown
## 716.3 GPIO_EXT Registers

The addresses in this section are relative to (GPIO base address + 0xOF00). GPIO base address is provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 7.22. GPIO_EXT_SIGMADELTA_n_REG (n: 0-3) (0x0000+0x4*n)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|--------------------------------|-----------------------------------------------------------------------------|
| 15        | Oxff                           |                                                                             |
| 8         | GPIO_EXT_SDn_PRESCALE         | Configures the divider value to divide IO MUX operating clock. (R/W)       |
| 7-0       | GPIO_EXT_SDn_IN                | Configures the duty cycle of sigma delta modulation output. (R/W)           |

### Register 7.23. GPIO_EXT_SIGMADELTA_MISC_REG (0x0024)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|--------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                    |                                                                             |
| 30-29     | GPIO_EXT_SD_FUNCTION_CLK_EN   | Configures whether or not to enable the clock for sigma delta modulation.    |
|           |                                | O: Not enable                                                                |
|           |                                | 1: Enable                                                                    |
|           |                                | (R/W)                                                                        |
```