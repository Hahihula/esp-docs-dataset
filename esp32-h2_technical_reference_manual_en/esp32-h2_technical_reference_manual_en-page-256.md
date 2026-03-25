

```markdown
Register 6.21. IO_MUX_DATE_REG (0x00FC)

IO_MUX_DATE_REG Version control register. (R/W)


6.18.3 GPIO_EXT Registers

The addresses in this section are relative to (GPIO base address + 0xOF00). GPIO base address is provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 6.22. GPIO_EXT_SIGMADELTA_REG (n: 0-3) (0x0000+0x4*n)

GPIO_EXT_SDO_IN Configures the duty cycle of sigma delta modulation output. (R/W)
GPIO_EXT_SDO_PRESCALE Configures the divider value to divide IO MUX operating clock. (R/W)


Register 6.23. GPIO_EXT_SIGMADELTA_MISC_REG (0x0024)

GPIO_EXT_SD_FUNCTION_CLK_EN Configures whether or not to enable the clock for sigma delta modulation.
O: Not enable
1: Enable
(R/W)
```