

```markdown
Register 2.100. cpu_gpio_out (0x805)

CPU_GPIO_OUT Configures GPIO(n = 0 ~ 21) output value. It is a CPU CSR to write value (1=high, 0=low) to SoC GPIO pin. The value takes effect only when CPU_GPIO_OEN is set.
CPU_GPIO_OUT[7:0] correspond to output signals cpu_gpio_out[7:0] in Table 8.12-1 Peripheral Signals via GPIO Matrix.
CPU_GPIO_OUT[7:0] can only be mapped to GPIO pins through GPIO matrix. For details please refer to Section 8.5 in Chapter GPIO Matrix and IO MUX.
(R/W)
```