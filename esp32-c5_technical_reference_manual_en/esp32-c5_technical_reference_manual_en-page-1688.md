

```markdown
Chapter 44 BitScrambler



Register 44.12. BITSCRAMBLER_RX_CTRL_REG (0x002C)

Continued from the previous page...

BITSCRAMBLER_RX_HALT_MODE Configures BitScrambler RX path halt mode when BITSCRAM-
BLER_RX_HALT is set to 1.
O: Wait for write data back done
    1: Ignore write data back
(R/W)

BITSCRAMBLER_RX_RD_DUMMY Configures BitScrambler RX path read data mode when EOF re-
ceived.
O: Wait read data
    1: Ignore read data
(R/W)

BITSCRAMBLER_RX_FIFO_RST Configures whether to reset BitScrambler RX FIFO.
O: Not reset
1: Reset
(WT)



Register 44.13. BITSCRAMBLER_SYS_REG (0x00F8)
```