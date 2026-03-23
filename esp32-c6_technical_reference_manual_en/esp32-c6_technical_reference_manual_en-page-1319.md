

```markdown
Register 37.5. RMT_SYS_CONF_REG (0x0068)

| Bit | 31 | 30 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | RMT_CLK_EN | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | (reserved) | RMT_MEM_FORCE_PU | RMT_MEM_FORCE_PD | RMT_MEM_CLK_FORCE_ON | RMT_APB_FIFO_MASK |
| Value | 0 | 0 | 0 | 0 | 1 | 0x1 | 0x0 | 0x0 | 0x0 | 0x1 | 0 | 0 | 0 | 0 | Reset |

RMT_APB_FIFO_MASK Configures the memory access mode.
- 0: Access memory by FIFO
- 1: Access memory directly (R/W)

RMT_MEM_CLK_FORCE_ON Configures whether to enable the clock for RMT memory.
- 0: Disable
- 1: Enable (R/W)

RMT_MEM_FORCE_PD Configures whether to power down RMT memory.
- 0: No effect
- 1: Power down (R/W)

RMT_MEM_FORCE_PU Configures whether to disable the power-down function of RMT memory in Light-sleep.
- 0: Power down RMT memory when RMT is in Light-sleep mode
- 1: Disable the power-down function of RMT memory in Light-sleep (R/W)

RMT_CLK_EN Configures whether to enable signal of RMT register clock gate.
- 0: Power down the drive clock of registers
- 1: Power up the drive clock of registers (R/W)
```