

```markdown
## Register 38.6. PARL_IO_INT_ENA_REG (0x0014)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   | Reset |    |

PARL_IO_TX_FIFO_REMPTY_INT_ENA Write 1 to enable TX_FIFO_REMPTY_INT. (R/W)
PARL_IO_RX_FIFO_WFULL_INT_ENA Write 1 to enable RX_FIFO_WFULL_INT. (R/W)
PARL_IO_TX_EOF_INT_ENA Write 1 to enable TX_EOF_INT. (R/W)

## Register 38.7. PARL_IO_INT_RAW_REG (0x0018)

| Bit 31 | ... | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|
|        |     |   |   | Reset |    |

PARL_IO_TX_FIFO_REMPTY_INT_RAW The raw interrupt status of TX_FIFO_REMPTY_INT. (R/SS/WTC)
PARL_IO_RX_FIFO_WFULL_INT_RAW The raw interrupt status of RX_FIFO_WFULL_INT. (R/SS/WTC)
PARL_IO_TX_EOF_INT_RAW The raw interrupt status of TX_EOF_INT. (R/SS/WTC)
```