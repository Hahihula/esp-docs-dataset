

```markdown
| Name                                       | Description                          | Address   | Access |
|--------------------------------------------|--------------------------------------|-----------|--------|
| INTMTX_COREO_SHA_INTR_MAP_REG             | SHA_INTR mapping register            | 0x00F4    | R/W    |
| INTMTX_COREO_RSA_INTR_MAP_REG             | RSA_INTR mapping register            | 0x00F8    | R/W    |
| INTMTX_COREO_ECC_INTR_MAP_REG             | ECC_INTR mapping register            | 0x00FC    | R/W    |
| INTMTX_COREO_ECDSA_INTR_MAP_REG           | ECDSA_INTR mapping register          | 0x0100    | R/W    |

Interrupt Status Registers
---------------------------

| Name                                       | Description                          | Address   | Access |
|--------------------------------------------|--------------------------------------|-----------|--------|
| INTMTX_COREO_INT_STATUS_0_REG             | Status register for interrupt sources 0 ~ 31 | 0x0104    | RO     |
| INTMTX_COREO_INT_STATUS_1_REG             | Status register for interrupt sources 32 ~ 63 | 0x0108    | RO     |
| INTMTX_COREO_INT_STATUS_2_REG             | Status register for interrupt source 64   | 0x010C    | RO     |

Version Control Registers
--------------------------

| Name                                       | Description                          | Address   | Access |
|--------------------------------------------|--------------------------------------|-----------|--------|
| INTMTX_COREO_INTERRUPT_REG_DATE_REG       | Version control register             | 0x07FC    | R/W    |

9.6.2 Interrupt Priority Register Summary

The addresses in this section are relative to the interrupt priority base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                          | Address   | Access |
|--------------------------------------------|--------------------------------------|-----------|--------|
| Configuration Registers                    |                                      |           |        |
| INTPRI_COREO_CPU_INT_ENABLE_REG           | Enable register for CPU interrupts    | 0x0000    | R/W    |
| INTPRI_COREO_CPU_INT_TYPE_REG             | Type configuration register for CPU interrupts | 0x0004    | R/W    |
| INTPRI_COREO_CPU_INT_EIP_STATUS_REG       | Pending status register for CPU interrupts | 0x0008    | RO     |
| INTPRI_COREO_CPU_INT_PRI_0_REG            | Priority configuration register for CPU interrupt 0 | 0x000C    | R/W    |
| INTPRI_COREO_CPU_INT_PRI_1_REG            | Priority configuration register for CPU interrupt 1 | 0x0010    | R/W    |
| INTPRI_COREO_CPU_INT_PRI_2_REG            | Priority configuration register for CPU interrupt 2 | 0x0014    | R/W    |
| INTPRI_COREO_CPU_INT_PRI_3_REG            | Priority configuration register for CPU interrupt 3 | 0x0018    | R/W    |
| INTPRI_COREO_CPU_INT_PRI_4_REG            | Priority configuration register for CPU interrupt 4 | 0x001C    | R/W    |
| INTPRI_COREO_CPU_INT_PRI_5_REG            | Priority configuration register for CPU interrupt 5 | 0x0020    | R/W    |
| INTPRI_COREO_CPU_INT_PRI_6_REG            | Priority configuration register for CPU interrupt 6 | 0x0024    | R/W    |
```