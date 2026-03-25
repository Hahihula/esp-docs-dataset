

```markdown
Register 9.62. INTMTX_COREO_INTMTX_DATE_REG (0x07FC)

| 31 | 28 | 27 | [reserved] |
|-----|-----|-----|------------|
| 0   | 0   | 0   |            |

0x2312061 Reset

INTMTX_COREO_INTMTX_DATE Version control register. (R/W)

## 9.7.2 Software Interrupt Registers

The addresses in this section are relative to the software interrupt base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 9.63. INTPRI_CPU_INTR_FROM_CPU_n_REG (n: 0-3) (0x0090+0x4*n)

| 31 | [reserved] |
|----|------------|
| 0  |            |

INTPRI_CPU_INTR_FROM_CPU_n CPU_INTR_FROM_CPU_n mapping register. Configures whether to generate interrupts by configuring the register through software.
0: Stop generating interrupts
1: Generate interrupts
(R/W)

Register 9.64. INTPRI_DATE_REG (0x00AO)

| 31 | 28 | 27 | [reserved] |
|----|----|----|------------|
| 0  | 0  | 0  |            |

0x2303150 Reset

INTPRI_DATE Version control register. (R/W)
```