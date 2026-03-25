

```markdown
Register 43.9. PARL_IO_REG_UPDATE_REG (0x0020)

PARL_IO_RX_REG_UPDATE Configures whether to update RX register configuration.
O: No effect
1: Update
(WT)
```

```markdown
Register 43.10. PARL_IO_ST_REG (0x0024)

PARL_IO_TX_READY Represents whether TX is ready to transmit data.
O: Not ready
1: Ready
(RO)
```

```markdown
Register 43.11. PARL_IO_INT_ENA_REG (0x0028)

PARL_IO_TX_FIFO_REMPTY_INT_ENA Write 1 to enable TX_FIFO_REMPTY_INT. (R/W)
PARL_IO_RX_FIFO_WOVF_INT_ENA Write 1 to enable RX_FIFO_WOVF_INT. (R/W)
PARL_IO_TX_EOF_INT_ENA Write 1 to enable TX_EOF_INT. (R/W)
```