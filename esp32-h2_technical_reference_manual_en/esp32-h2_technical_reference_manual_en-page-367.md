

```markdown
Register 9.63. INTPRI_COREO_CPU_INT_PRI_n_REG (n: 0-31) (0x000C+0x4*n)

| Bit 31 | ... | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|
|        |     |   |   |   |   | Reset |

INTPRI_COREO_CPU_PRI_n_MAP Configures the priority for CPU interrupt n. The priority here can be 1 (lowest) ~ 15 (highest). For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU > Section 1.6 Interrupt Controller. (R/W)

Register 9.64. INTPRI_COREO_CPU_INT_THRESH_REG (0x008C)

| Bit 31 | ... | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|---|---|---|---|
|        |     |   |   |   |   |   |   |   |   | Reset |

INTPRI_COREO_CPU_INT_THRESH Configures the threshold for interrupt assertion to CPU. Only when the interrupt priority is equal to or higher than this threshold, CPU will respond to this interrupt. For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU > Section 1.6 Interrupt Controller. (R/W)
```