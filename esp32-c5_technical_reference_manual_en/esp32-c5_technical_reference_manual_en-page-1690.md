

```markdown
Register 44.15. BITSCRAMBLER_RX_STATE_REG (0x0034)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 30   | 29                         | 16 | 15 | 5 | 4 | 3 | 2 | 1 | 0    |
| 0   | 0    | 0                         | 0  | 0  | 0 | 0 | 0 | 0 | 0 | Reset |

BITSCRAMBLER_RX_IN_IDLE Represents whether BitScrambler TX path is halted.
- O: Not halted
- 1: Halted (RO)

BITSCRAMBLER_RX_IN_RUN Represents whether BitScrambler TX path is running.
- O: Not running
- 1: Running (RO)

BITSCRAMBLER_RX_IN_WAIT Represents whether BitScrambler TX path is waiting for write back done.
- O: Not waiting
- 1: Waiting (RO)

BITSCRAMBLER_RX_IN_PAUSE Represents whether BitScrambler TX path is paused.
- O: Not paused
- 1: Paused (RO)

BITSCRAMBLER_RX_FIFO_FULL Represents whether BitScrambler RX FIFO is full.
- O: Not full
- 1: Full (RO)

BITSCRAMBLER_RX_EOF_GET_CNT Represents byte count of BitScrambler TX path after EOF is received. (RO)

BITSCRAMBLER_RX_EOF_OVERLOAD Represents whether BitScrambler RX path tries to process more than one EOF.
- O: Not try to process more than one EOF
- 1: Try to process more than one EOF (RO)

BITSCRAMBLER_RX_EOF_TRACE_CLR Configures whether to clear BITSCRAMBLER_RX_EOF_OVERLOAD and BITSCRAMBLER_RX_EOF_GET_CNT.
- O: Not clear
- 1: Clear (WT)
```