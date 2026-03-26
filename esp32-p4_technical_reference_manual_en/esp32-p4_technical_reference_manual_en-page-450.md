

```markdown
Register 6.36. DMA2D_EXTR_MEM_END_ADDR_REG (0x0A14)

DMA2D_ACCESS_EXTR_MEM_END_ADDR   Configures the end address of the accessible external address space. Accessing an address beyond this range will result in a descriptor error. (R/W)

Register 6.37. DMA2D_OUT_ARB_CONFIG_REG (0x0A18)

DMA2D_OUT_ARB_TIMEOUT_NUM   Configures the time slot for TX. Measurement unit: AXI bus clock cycle. (R/W)

DMA2D_OUT_WEIGHT_EN   Configures whether to enable weight arbitration for TX.
  0: Disable
  1: Enable
(R/W)
```