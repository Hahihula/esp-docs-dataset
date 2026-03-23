

```markdown
Register 10.66. INTPRI_COREO_CPU_INT_EIP_STATUS_REG (0x0008)

INTPRI_COREO_CPU_INT_EIP_STATUS Represents the pending status of CPU interrupts. For more information about how to use this register, see Chapter 1 High-Performance CPU. (RO)


Register 10.67. INTPRI_COREO_CPU_INT_PRI_n_REG (n: 0-31) (0x000C+0x4*n)

INTPRI_COREO_CPU_PRI_n_MAP Configures the priority for CPU interrupt n. The priority here can be 1 (lowest) ~ 15 (highest). For more information about how to use this register, see Chapter 1 High-Performance CPU. (R/W)


Register 10.68. INTPRI_COREO_CPU_INT_THRESH_REG (0x008C)

INTPRI_COREO_CPU_INT_THRESH Configures the threshold for interrupt assertion to CPU. Only when the interrupt priority is equal to or higher than this threshold, CPU will respond to this interrupt. For more information about how to use this register, see Chapter 1 High-Performance CPU. (R/W)
```