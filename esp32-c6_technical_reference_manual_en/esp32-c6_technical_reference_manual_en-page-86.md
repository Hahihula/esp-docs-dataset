

```markdown
| Name               | Description                  | Address | Access |
|--------------------|------------------------------|---------|--------|
| cpu_gpio_oen       | GPIO Output Enable           | 0x803   | R/W    |
| cpu_gpio_in        | GPIO Input Value             | 0x804   | RO     |
| cpu_gpio_out       | GPIO Output Value            | 0x805   | R/W    |

### 1.14.5 Register Description

Register 1.46. `cpu_gpio_oen` (0x803)

CPU_GPIO_OEN Configures whether to enable GPIO(n=0 ~ 21) output. CPU_GPIO_OEN[7:0] correspond to output enable signals cpu_gpio_out_oen[7:0] in Table 7.11-1 Peripheral Signals via GPIO Matrix. CPU_GPIO_OEN value matches that of cpu_gpio_out_open. CPU_GPIO_OEN is the enable signal of CPU_GPIO_OUT.
0: Disable GPIO output
1: Enable GPIO output (R/W)

Register 1.47. `cpu_gpio_in` (0x804)

CPU_GPIO_IN Represents GPIO(n=0 ~ 21) input value. It is a CPU CSR to read input value (1=high, 0=low) from SoC GPIO pin.
CPU_GPIO_IN[7:0] correspond to input signals cpu_gpio_in[7:0] in Table 7.11-1 Peripheral Signals via GPIO Matrix.
CPU_GPIO_IN[7:0] can only be mapped to GPIO pins through GPIO matrix. For details please refer to Section 7.4 in Chapter IO MUX and GPIO Matrix (GPIO, IO MUX).
(RO)
```