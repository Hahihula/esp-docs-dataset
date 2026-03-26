

```markdown
Chapter 59 BitScrambler GoBack

Register 59.11. BITSCRAMBLER_TX_CTRL_REG (0x0028)

| bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | Reset |

BITSCRAMBLER_TX_ENA Configures whether to enable BitScrambler TX core.
O: Disable
1: Enable
(R/W)

BITSCRAMBLER_TX_PAUSE Configures whether to pause BitScrambler TX core. A paused core can be un-paused to resume execution.
O: Not pause
1: Pause
(R/W)

BITSCRAMBLER_TX_HALT Configures whether to halt BitScrambler TX core. Halting the BitScrambler TX core will flush the FIFOs and cannot be resumed; a FIFO reset and a restart is needed.
O: Not halt
1: Halt (R/W)

BITSCRAMBLER_TX_EOF_MODE Configures BitScrambler TX core EOF signal generating mode. This is combined with BITSCRAMBLER_TX_TAILING_BITS for use.
O: Data written to the output FIFO are counted to generate delayed EOF
1: Data read from the input FIFO are counted to generate delayed EOF
(R/W)

BITSCRAMBLER_TX_COND_MODE Configures BitScrambler TX LOOP instruction condition mode.
O: Use the less than operator to get the condition
1: Use not equal operator to get the condition
(R/W)

BITSCRAMBLER_TX_FETCH_MODE Configures BitScrambler TX core fetch instruction mode.
O: Prefetch by reset
1: Fetch by instructions
(R/W)

BITSCRAMBLER_TX_HALT_MODE Configures BitScrambler TX core halt mode when BITSCRAMBLER_TX_HALT is set
O: Wait for write data back done
1: Ignore write data back
(R/W)

Continued on the next page...
```