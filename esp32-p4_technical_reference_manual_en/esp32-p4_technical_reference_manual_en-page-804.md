

```markdown
Chapter 12 Interrupt Matrix

Register 12.129. COREO_SOURCE_MAP_REG (0x0000 - 0x01FC, 0x0214 - 0x021C)

COREO_SOURCE_MAP    When COREO_SOURCE_SRC_IN_SEC_FLAG is set to 1, this register can only be written by CPU while in Machine Mode.

Configure this register to map the interrupt signal from the peripheral interrupt sources Source to one of CPU0's peripheral interrupts. The valid configuration range is 16 ~ 47.
When set to 0 ~ 15, the corresponding peripheral interrupt source is disabled (recommended value: 0).
Other values are invalid.
For the list of interrupt sources Source, see Table 12.4-1. (R/W)

COREO_SOURCE_SRC_PASS_IN_SEC Write 1 to allow the interrupt signal from interrupt source Source to be delegated to CPU0's Machine Mode interrupt. Writable only by the CPU in Machine Mode. (R/W)

COREO_SOURCE_SRC_IN_SEC_FLAG Write 1 to configure the interrupt signal from interrupt source Source as a secure interrupt source (that is, its interrupt mapping can be configured only by the CPU running in Machine Mode). Writable only by the CPU in Machine Mode. (R/W)

Register 12.130. COREO_INTR_STATUS_REG_O_REG (0x0200)
```
```markdown
COREO_INTR_STATUS_O Represents the status of the interrupt sources from 0 ~ 31. Each bit corresponds to one interrupt source. (RO)
```