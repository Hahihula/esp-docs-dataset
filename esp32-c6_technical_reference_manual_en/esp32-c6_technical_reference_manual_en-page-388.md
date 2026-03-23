

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| INTMTX_COREO_DMA_OUT_CHO_INTR_MAP_REG     | GDMA_OUT_CHO_INTR mapping register                                         | 0x0114  | R/W    |
| INTMTX_COREO_DMA_OUT_CH1_INTR_MAP_REG     | GDMA_OUT_CH1_INTR mapping register                                        | 0x0118  | R/W    |
| INTMTX_COREO_DMA_OUT_CH2_INTR_MAP_REG     | GDMA_OUT_CH2_INTR mapping register                                        | 0x011C  | R/W    |
| INTMTX_COREO_GPSPI2_INTR_MAP_REG           | GPSPI2_INTR mapping register                                              | 0x0120  | R/W    |
| INTMTX_COREO_AES_INTR_MAP_REG              | AES_INTR mapping register                                                 | 0x0124  | R/W    |
| INTMTX_COREO_SHA_INTR_MAP_REG              | SHA_INTR mapping register                                                 | 0x0128  | R/W    |
| INTMTX_COREO_RSA_INTR_MAP_REG              | RSA_INTR mapping register                                                 | 0x012C  | R/W    |
| INTMTX_COREO_ECC_INTR_MAP_REG              | ECC_INTR mapping register                                                 | 0x0130  | R/W    |

**Interrupt Status Register**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| INTMTX_COREO_INT_STATUS_O_REG             | Status register for interrupt sources 0 ~ 31                               | 0x0134  | RO     |
| INTMTX_COREO_INT_STATUS_1_REG              | Status register for interrupt sources 32 ~ 63                              | 0x0138  | RO     |
| INTMTX_COREO_INT_STATUS_2_REG              | Status register for interrupt sources 64 ~ 76                              | 0x013C  | RO     |

**Version Control Register**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| INTMTX_COREO_INTERRUPT_REG_DATE_REG        | Version control register                                                   | 0x07FC  | R/W    |

## 10.4.2 Interrupt Priority Register Summary

The addresses in this section are relative to the interrupt priority base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Configuration Registers**                |                                                                             |         |        |
| INTPRI_COREO_CPU_INT_ENABLE_REG            | Enable register for CPU interrupts                                        | 0x0000  | R/W    |
| INTPRI_COREO_CPU_INT_TYPE_REG              | Type configuration register for CPU interrupts                            | 0x0004  | R/W    |
| INTPRI_COREO_CPU_INT_EIP_STATUS_REG        | Pending status register for CPU interrupts                                 | 0x0008  | RO     |
| INTPRI_COREO_CPU_INT_PRI_O_REG             | Priority configuration register for CPU interrupt 0                       | 0x000C  | R/W    |
| INTPRI_COREO_CPU_INT_PRI_1_REG             | Priority configuration register for CPU interrupt 1                       | 0x0010  | R/W    |
| INTPRI_COREO_CPU_INT_PRI_2_REG             | Priority configuration register for CPU interrupt 2                       | 0x0014  | R/W    |
```