

```markdown
Register 58.14. PARL_IO_INT_CLR_REG (0x0034)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   |   | Reset |

PARL_IO_TX_FIFO_REMPTY_INT_CLR Write 1 to clear TX_FIFO_REMPTY_INT. (WT)
PARL_IO_RX_FIFO_WOVF_INT_CLR Write 1 to clear RX_FIFO_WOVF_INT. (WT)
PARL_IO_TX_EOF_INT_CLR Write 1 to clear TX_EOF_INT. (WT)

Register 58.15. PARL_IO_RX_STO_REG (0x0038)

| Bit 31 | ... | 13 | 12 | 8 | 7 | 0 |
|--------|-----|-----|-----|---|---|---|
|        |     |     |     |   |   | Reset |

PARL_IO_RX_CNT Represents the clock cycle number of reading the RX FIFO. (RO)
PARL_IO_RX_FIFO_WR_BIT_CNT Represents the bit number currently written into the RX FIFO. (RO)

Register 58.16. PARL_IO_RX_ST1_REG (0x003C)

| Bit 31 | ... | 13 | 12 | 0 |
|--------|-----|-----|-----|---|
|        |     |     |     | Reset |

PARL_IO_RX_FIFO_RD_BIT_CNT Represents the bit number currently read from the RX FIFO. (RO)
```