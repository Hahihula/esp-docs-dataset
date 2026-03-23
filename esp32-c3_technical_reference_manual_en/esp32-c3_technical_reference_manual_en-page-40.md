

```markdown
Register 1.14. mpccr (0x7E2)

MPCCR Machine Performance Counter Value. (R/W)


Register 1.15. cpu_gpio_oen (0x803)

CPU_GPIO_OEN GPIOOn (n=0 ~ 21) Output Enable. CPU_GPIO_OEN[7:0] correspond to output enable signals cpu_gpio_out_oen[7:0] in Table 5.11-1 Peripheral Signals via GPIO Matrix.
CPU_GPIO_OEN value matches that of cpu_gpio_out_oen.
CPU_GPIO_OEN is the enable signal of CPU_GPIO_OUT. (R/W)

*   0: GPIO output disable
*   1: GPIO output enable


Register 1.16. cpu_gpio_in (0x804)

CPU_GPIO_IN GPIOIn (n=0 ~ 21) Input Value. It is a CPU CSR to read input value (1=high, 0=low) from SoC GPIO pin.
CPU_GPIO_IN[7:0] correspond to input signals cpu_gpio_in[7:0] in Table 5.11-1 Peripheral Signals via GPIO Matrix.
CPU_GPIO_IN[7:0] can only be mapped to GPIO pins through GPIO matrix. For details please refer to Section 5.4 in Chapter IO MUX and GPIO Matrix (GPIO, IO MUX). (RO)
```