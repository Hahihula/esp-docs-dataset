

```markdown
Register 1.17. cpu_gpio_out (0x805)

CPU_GPIO_OUT GPIO[n=0 ~ 21) Output Value. It is a CPU CSR to write value (1=high, O=low) to SoC GPIO pin. The value takes effect only when CPU_GPIO_OEN is set.
CPU_GPIO_OUT[7:0] correspond to output signals cpu_gpio_out[7:0] in Table 5.11-1 Peripheral Signals via GPIO Matrix
CPU_GPIO_OUT[7:0] can only be mapped to GPIO pins through GPIO matrix. For details please refer to Section 5.5 in Chapter IO MUX and GPIO Matrix (GPIO, IO MUX). (R/W)
```