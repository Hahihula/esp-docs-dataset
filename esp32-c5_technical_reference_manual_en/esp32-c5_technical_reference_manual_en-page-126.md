

```markdown
## 2.12.2.4 Register Summary

Below is a list of custom dedicated IO CSRs implemented inside the core.

| Name               | Description          | Address | Access |
|--------------------|----------------------|---------|--------|
| cpu_gpio_oen       | GPIO Output Enable   | 0x803   | R/W    |
| cpu_gpio_in        | GPIO Input Value     | 0x804   | RO     |
| cpu_gpio_out       | GPIO Output Value    | 0x805   | R/W    |

## 2.12.2.5 Register Description

Register 2.98. `cpu_gpio_oen` (0x803)

```
┌──────────────────────────────────────────────────────────────────────────────┐
│ 31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0 │
│  └────────────────────────────────────────────────────────────────────────────┘
│   (reserved) CPU_GPIO_OEN[7:0]                                                |
└──────────────────────────────────────────────────────────────────────────────┘

CPU_GPIO_OEN Configures whether to enable GPIO(n=0 ~ 21) output. CPU_GPIO_OEN[7:0] correspond to output enable signals cpu_gpio_out_oen[7:0] in Table 8.12-1 Peripheral Signals via GPIO Matrix. CPU_GPIO_OEN value matches that of cpu_gpio_out_oen. CPU_GPIO_OEN is the enable signal of CPU_GPIO_OUT.
O: Disable GPIO output
1: Enable GPIO output
(R/W)

Register 2.99. `cpu_gpio_in` (0x804)

```
┌──────────────────────────────────────────────────────────────────────────────┐
│ 31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0 │
│  └────────────────────────────────────────────────────────────────────────────┘
│   (reserved) CPU_GPIO_IN[7:0]                                                 |
└──────────────────────────────────────────────────────────────────────────────┘

CPU_GPIO_IN Represents GPIO(n=0 ~ 21) input value. It is a CPU CSR to read input value (1=high, O=low) from SoC GPIO pin.
CPU_GPIO_IN[7:0] correspond to input signals cpu_gpio_in[7:0] in Table 8.12-1 Peripheral Signals via GPIO Matrix.
CPU_GPIO_IN[7:0] can only be mapped to GPIO pins through GPIO matrix. For details please refer to Section 8.4 in Chapter GPIO Matrix and IO MUX.
(RO)
```