

```markdown
Register 10.62. INTMTX_COREO_INT_STATUS_2_REG (0x013C)

INTMTX_COREO_INT_STATUS_2    Represents the status of the interrupt sources numbered from 64 ~ 76. Bit 0 ~ 12 each corresponds to one interrupt source. Other bits are invalid.
0: The corresponding interrupt source triggered an interrupt
1: No interrupt triggered
(RO)

Register 10.63. INTMTX_COREO_INTERRUPT_REG_DATE_REG (0x07FC)

INTMTX_COREO_INTERRUPT_REG_DATE    Version control register. (R/W)
```

## 10.5.2 Interrupt Priority Registers

The addresses in this section are relative to the interrupt priority base address provided in Table 5.3-2 in Chapter 5 System and Memory.
```