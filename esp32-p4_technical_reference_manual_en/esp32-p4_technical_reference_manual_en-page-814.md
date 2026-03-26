

```markdown
Register 12.272. CORE1_AXI_PERF_MON_INT_MAP_REG (0x021C)

Register 12.273. CORE1_SOURCE_MAP_REG (0x0000 - 0x01FC, 0x0214 - 0x021C)
```
```markdown
CORE1_SOURCE_MAP  When CORE1_SOURCE_SRC_IN_SEC_FLAG is set to 1, this register can only be written by CPU while in Machine Mode.

Configures this register to map the interrupt signal from the peripheral interrupt sources Source to one of CPU1's peripheral interrupts. The valid configuration range is 16 ~ 47.
When set to 0 ~ 15, the corresponding peripheral interrupt source is disabled (recommended value: 0).

Other values are invalid.

For the list of interrupt sources Source, see Table 12.4-1. (R/W)
```
```markdown
CORE1_SOURCE_SRC_PASS_IN_SEC Write 1 to allow the interrupt signal from interrupt source Source to be delegated to CPU1's Machine Mode interrupt. Writable only by the CPU in Machine Mode. (R/W)

CORE1_SOURCE_SRC_IN_SEC_FLAG Write 1 to configure the interrupt signal from interrupt source Source as a secure interrupt source (that is, its interrupt mapping can be configured only by the CPU running in Machine Mode). Writable only by the CPU in Machine Mode. (R/W)
```
```markdown
Register 12.274. CORE1_INTR_STATUS_REG_O_REG (0x0200)

CORE1_INTR_STATUS_O Represents the status of the interrupt sources from 0 ~ 31. Each bit corresponds to one interrupt source. (RO)
```