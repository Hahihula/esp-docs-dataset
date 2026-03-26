

```markdown
Chapter 59 BitScrambler

Register 59.12. BITSCRAMBLER_RX_CTRL_REG (0x002C)

Continued from the previous page...

BITSCRAMBLER_RX_HALT_MODE Configures BitScrambler RX core halt mode when BITSCRAM-
BLER_RX_HALT is set
O: Wait for write data back done
1: Ignore write data back
(R/W)

BITSCRAMBLER_RX_RD_DUMMY Configures BitScrambler RX core read data mode when EOF re-
ceived.
O: Wait read data
1: Ignore read data
(R/W)

BITSCRAMBLER_RX_FIFO_RST Configures whether to reset BitScrambler RX FIFO.
O: Not reset
1: Reset
(WT)

Register 59.13. BITSCRAMBLER_SYS_REG (0x00F8)
```
```markdown
| 31 | 30                                                                                                                                                                                                 | 1 | 0 |
|----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|---|
|    | O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O O | Reset |
|    |                                                                                                                                                                                                 |     |
```
```markdown
BITSCRAMBLER_LOOP_MODE Configures whether to enable BitScrambler TX to DMA RX loopback mode
O: Disable
1: Enable
(R/W)

BITSCRAMBLER_CLK_EN Reserved. (R/W)
```