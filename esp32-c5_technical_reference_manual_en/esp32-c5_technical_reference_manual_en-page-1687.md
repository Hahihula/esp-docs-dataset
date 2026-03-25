

```markdown
Chapter 44 BitScrambler

Register 44.12. BITSCRAMBLER_RX_CTRL_REG (0x002C)

| 31 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

BITSCRAMBLER_RX_ENA Configures whether to enable the BitScrambler core in the RX path.
- 0: Disable
- 1: Enable

Note that the BitScrambler core can only be enabled either in the RX or TX path, never both.
(R/W)

BITSCRAMBLER_RX_PAUSE Configures whether to pause BitScrambler RX path. A paused core can be un-paused to resume execution.
- 0: Not pause
- 1: Pause
(R/W)

BITSCRAMBLER_RX_HALT Configures whether to halt BitScrambler RX path. Halting the BitScrambler RX path will flush the FIFOs and cannot be resumed; a FIFO reset and a restart is needed.
- 0: Not halt
- 1: Halt
(R/W)

BITSCRAMBLER_RX_EOF_MODE Configures BitScrambler RX path EOF signal generating mode. This is combined with BITSCRAMBLER_RX_TAILING_BITS for use.
- 0: Data written to the output FIFO are counted to generate delayed EOF
- 1: Data read from the input FIFO are counted to generate delayed EOF
(R/W)

BITSCRAMBLER_RX_COND_MODE Configures BitScrambler RX LOOP instruction condition mode.
- 0: Use the less than operator to get the condition
- 1: Use not equal operator to get the condition
(R/W)

BITSCRAMBLER_RX_FETCH_MODE Configures BitScrambler RX path fetch instruction mode
- 0: Prefetch by reset
- 1: Fetch by instructions
(R/W)

Continued on the next page...
```