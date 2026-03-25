

```markdown
Register 9.65. INTPRI_COREO_CPU_INT_CLEAR_REG (0x00A8)

INTPRI_COREO_CPU_INT_CLEAR Configures whether to clear the corresponding CPU interrupt.
- 0: No effect
- 1: Clear

For more information about how to use this register, see Chapter 1 ESP-RISC-V CPU > Section 1.6 Interrupt Controller.

(R/W)
```

```markdown
Register 9.66. INTPRI_CPU_INTR_FROM_CPU_n_REG (n: 0-3) (0x0090+0x4*n)

INTPRI_CPU_INTR_FROM_CPU_n Configures whether to generate interrupts from CPU_INTR_FROM_CPU_n.
- 0: Do not generate interrupts
- 1: Generate interrupts

(R/W)
```

```markdown
Register 9.67. INTPRI_DATE_REG (0x00A0)

INTPRI_DATE Version control register. (R/W)
```