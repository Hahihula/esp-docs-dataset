

```markdown
| Name                              | Description                          | Address | Access |
|------------------------------------|--------------------------------------|---------|--------|
| INTMTX_COREO_INTMTX_DATE_REG      | Version control register             | 0x07FC  | R/W    |

## 11.6.2 Software Interrupt Register Summary

The addresses in this section are relative to the software interrupt base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                              | Description                          | Address | Access |
|------------------------------------|--------------------------------------|---------|--------|
| **Interrupt Registers**            |                                      |         |        |
| INTPRI_CPU_INTR_FROM_CPU_0_REG    | CPU_INTR_FROM_CPU_0 mapping register| 0x0090  | R/W    |
| INTPRI_CPU_INTR_FROM_CPU_1_REG     | CPU_INTR_FROM_CPU_1 mapping register| 0x0094  | R/W    |
| INTPRI_CPU_INTR_FROM_CPU_2_REG     | CPU_INTR_FROM_CPU_2 mapping register| 0x0098  | R/W    |
| INTPRI_CPU_INTR_FROM_CPU_3_REG     | CPU_INTR_FROM_CPU_3 mapping register| 0x009C  | R/W    |
| **Version Registers**              |                                      |         |        |
| INTPRI_DATE_REG                   | Version control register             | 0x00A0  | R/W    |
```