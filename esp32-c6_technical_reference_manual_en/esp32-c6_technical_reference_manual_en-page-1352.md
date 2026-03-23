

```markdown
Register 38.8. PARL_IO_INT_ST_REG (0x001C)

| Bit 31 | ... | 2 | 1 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | Reset |

PARL_IO_TX_FIFO_REMPTY_INT_ST The masked interrupt status of TX_FIFO_REMPTY_INT. (RO)
PARL_IO_RX_FIFO_WFULL_INT_ST The masked interrupt status of RX_FIFO_WFULL_INT. (RO)
PARL_IO_TX_EOF_INT_ST The masked interrupt status of TX_EOF_INT. (RO)

Register 38.9. PARL_IO_INT_CLR_REG (0x0020)

| Bit 31 | ... | 2 | 1 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | Reset |

PARL_IO_TX_FIFO_REMPTY_INT_CLR Write 1 to clear TX_FIFO_REMPTY_INT. (WT)
PARL_IO_RX_FIFO_WFULL_INT_CLR Write 1 to clear RX_FIFO_WFULL_INT. (WT)
PARL_IO_TX_EOF_INT_CLR Write 1 to clear TX_EOF_INT. (WT)
```