

```markdown
## Chapter 38 Parallel IO Controller (PARL_IO)

Register 38.12. PARL_IO_INT_RAW_REG (0x002C)
```
![Register 38.12 Bit Diagram](image_path_if_available)  
*(Note: Actual diagram not rendered here, but described as per instruction to describe diagrams if understood or block/flowcharts)*

- `PARL_IO_TX_FIFO_REMPTY_INT_RAW` The raw interrupt status of TX_FIFO_REMPTY_INT. (R/WTC/SS)
- `PARL_IO_RX_FIFO_WOVF_INT_RAW` The raw interrupt status of RX_FIFO_WOVF_INT. (R/WTC/SS)
- `PARL_IO_TX_EOF_INT_RAW` The raw interrupt status of TX_EOF_INT. (R/WTC/SS)

Register 38.13. PARL_IO_INT_ST_REG (0x0030)
```
![Register 38.13 Bit Diagram](image_path_if_available)  
*(Note: Actual diagram not rendered here, but described as per instruction to describe diagrams if understood or block/flowcharts)*

- `PARL_IO_TX_FIFO_REMPTY_INT_ST` The masked interrupt status of TX_FIFO_REMPTY_INT. (RO)
- `PARL_IO_RX_FIFO_WOVF_INT_ST` The masked interrupt status of RX_FIFO_WOVF_INT. (RO)
- `PARL_IO_TX_EOF_INT_ST` The masked interrupt status of TX_EOF_INT. (RO)
```