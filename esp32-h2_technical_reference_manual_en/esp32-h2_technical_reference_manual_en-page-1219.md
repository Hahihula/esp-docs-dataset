

```markdown
Chapter 38 Parallel IO Controller (PARL_IO)

Register 38.9. PARL_IO_REG_UPDATE_REG (0x0020)
```
| Bit 31 | Bit 30 | ... | Bit 0 |
|--------|--------|-----|-------|
|        | `PARL_IO_RX_REG_UPDATE` | `(reserved)` | Reset |
```


PARL_IO_RX_REG_UPDATE Configures whether to update RX register configuration.  
O: No effect  
1: Update (WT)

Register 38.10. PARL_IO_ST_REG (0x0024)
```
| Bit 31 | Bit 30 | ... | Bit 0 |
|--------|--------|-----|-------|
|        | `PARL_IO_TX_READY` | `(reserved)` | Reset |
```


PARL_IO_TX_READY Represents whether TX is ready to transmit data.  
O: Not ready  
1: Ready (RO)

Register 38.11. PARL_IO_INT_ENA_REG (0x0028)
```
| Bit 31 | ... | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|-----|-------|-------|-------|-------|
|        | `(reserved)` | `PARL_IO_TX_EOF_INT_ENA` | `PARL_IO_RX_FIFO_WOVF_INT_ENA` | `PARL_IO_TX_FIFO_REMPTY_INT_ENA` | Reset |
```


PARL_IO_TX_FIFO_REMPTY_INT_ENA Write 1 to enable TX_FIFO_REMPTY_INT. (R/W)  
PARL_IO_RX_FIFO_WOVF_INT_ENA Write 1 to enable RX_FIFO_WOVF_INT. (R/W)  
PARL_IO_TX_EOF_INT_ENA Write 1 to enable TX_EOF_INT. (R/W)
```