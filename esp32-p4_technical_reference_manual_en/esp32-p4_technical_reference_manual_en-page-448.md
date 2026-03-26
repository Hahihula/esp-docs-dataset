

```markdown
Register 6.32. DMA2D_RST_CONF_REG (0x0A04)

DMA2D_AXIM_RD_RST Configures whether to reset the AXI master read data FIFO.
- 0: No effect
- 1: Reset
(R/W)

DMA2D_AXIM_WR_RST Configures whether to reset the AXI master write data FIFO.
- 0: No effect
- 1: Reset
(R/W)

DMA2D_CLK_EN Configures the clock for registers.
- 0: Support clock only when application writes registers
- 1: Force clock on for register
(R/W)
```

```markdown
Register 6.33. DMA2D_INTR_MEM_START_ADDR_REG (0x0A08)

DMA2D_ACCESS_INTR_MEM_START_ADDR Configures the start address of the accessible internal address space. (R/W)
```