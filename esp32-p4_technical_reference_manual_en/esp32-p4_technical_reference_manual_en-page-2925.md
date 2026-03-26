

```markdown
## 58.6 Interrupts

ESP32-P4's PARLIO module can generate the following interrupt signals that will be sent to the **Interrupt Matrix**.

*   `PARL_IO_TX_INTR`
*   `PARL_IO_RX_INTR`

There are several internal interrupt sources from PARLIO that can generate the above interrupt signals. The interrupt sources from PARLIO are listed with their trigger conditions and the resulted interrupt signals in Table 58.6-1.

Table 58.6-1. PARLIO's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                                                                 | Interrupt Signal   |
|----------------------------|------------------------------------------------------------------------------------|--------------------|
| TX_FIFO_REMPTY_INT         | TX FIFO is empty, indicating possible error in the data sent by TX                 | `PARL_IO_TX_INTR`  |
| RX_FIFO_WOVF_INT            | RX FIFO is full, indicating possible error in the data received by RX              | `PARL_IO_RX_INTR`  |
| TX_EOF_INT                  | TX finishes sending a complete frame of data                                       | `PARL_IO_TX_INTR`  |
```