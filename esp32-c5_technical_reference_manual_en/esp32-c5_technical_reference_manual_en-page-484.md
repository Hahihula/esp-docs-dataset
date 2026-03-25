

```markdown
Register 11.66. INTMTX_COREO_RSA_INTR_MAP_REG (0x140)
Register 11.67. INTMTX_COREO_ECC_INTR_MAP_REG (0x144)
Register 11.68. INTMTX_COREO_ECDSA_INTR_MAP_REG (0x148)
Register 11.69. INTMTX_COREO_KM_INTR_MAP_REG (0x14C)

Register 11.70. INTMTX_COREO_SOURCE_INTR_MAP_REG (0x0000 - 0x0100)

INTMTX_COREO_SOURCE_INTR_MAP   Map the INTMTX source (SOURCE) into one CPU INTMTX.
For the information of SOURCE, see Table 11.5-1. (R/W)

INTMTX_COREO_SOURCE_INTR_PASS_IN_SEC  Delegate the interrupt signal of the INTMTX
source (SOURCE) to a CPU Machine Mode interrupt.(R/W)

Register 11.71. INTMTX_COREO_INT_STATUS_O_REG (0x0150)

INTMTX_COREO_INT_STATUS_O  Represents the status of the INTMTX sources numbered from 0 ~ 31. Each bit corresponds to one INTMTX source.
0: No interrupt triggered from the corresponding INTMTX source
1: The corresponding INTMTX source triggered an interrupt (RO)
```