

```markdown
Register 54.1. CTRL_REG (0x0000)

Continued from the previous page...

SDHOST_CEATA_DEVICE_INTERRUPT_STATUS Write 1 to enable interrupts in CE-ATA device (nIEN = 0 in ATE control register).
Software should appropriately write to this bit after the power-on reset or any other reset to the CE-ATA device. After reset, the CE-ATA device's interrupt is usually disabled (nIEN = 1). If the host enables the CE-ATA device's interrupt, then software should set this bit. (R/W)

SDHOST_USE_INTERNAL_DMAC Configures whether to use DMA for data transfer.
0: Not use
1: Use
(R/W)

Register 54.2. SDHOST_CLKDIV_REG (0x0008)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----|----|----|----|----|---|---|---|
|    |    |    |    |    |   |   | Reset |
| 0x0 |    | 0x0 |    | 0x0 |   |   | 0x0 |

SDHOST_CLK_DIVIDERO Configures clock divider0 value. Clock divisor is 2*n, where n = 0 bypasses the divider (divisor of 1). For example, a value of 1 means divided by 2*1 = 2, a value of 0xFF means divided by 2*255 = 510, and so on. (R/W)

SDHOST_CLK_DIVIDER1 Configures clock divider1 value. Clock divisor is 2*n, where n = 0 bypasses the divider (divisor of 1). For example, a value of 1 means divided by 2*1 = 2, a value of 0xFF means divided by 2*255 = 510, and so on. (R/W)

SDHOST_CLK_DIVIDER2 Configures clock divider2 value. Clock divisor is 2*n, where n = 0 bypasses the divider (divisor of 1). For example, a value of 1 means divided by 2*1 = 2, a value of 0xFF means divided by 2*255 = 510, and so on. (R/W)

SDHOST_CLK_DIVIDER3 Configures clock divider3 value. Clock divisor is 2*n, where n = 0 bypasses the divider (divisor of 1). For example, a value of 1 means divided by 2*1 = 2, a value of 0xFF means divided by 2*255 = 510, and so on. (R/W)
```