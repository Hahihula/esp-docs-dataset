
```markdown
## 43.6 Interrupts

ESP32-C5's PARLIO module can generate the following interrupt signals that will be sent to the **Interrupt Matrix**.

- `PARL_IO_TX_INTR`
- `PARL_IO_RX_INTR`

There are several internal interrupt sources from PARLIO that can generate the above interrupt signals. The interrupt sources from PARLIO are listed with their trigger conditions and the resulted interrupt signals in Table 43.6-1.

Table 43.6-1. PARLIO's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition                                                                                      | Interrupt Signal         |
|----------------------------|--------------------------------------------------------------------------------------------------------|--------------------------|
| TX_FIFO_REMPTY_INT        | TX FIFO is empty, indicating possible error in the data sent by TX                                      | `PARL_IO_TX_INTR`       |
| RX_FIFO_WOVF_INT           | RX FIFO is full, indicating possible error in the data received by RX                                  | `PARL_IO_RX_INTR`       |
| TX_EOF_INT                 | TX finishes sending a complete frame of data                                                           | `PARL_IO_TX_INTR`       |

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 **Interrupt Matrix** > Section 11.2 Terminology.

Each interrupt source can be configured by a common set of registers that are described in Section **Interrupt Configuration Registers**. The specific registers can be found in Section 43.9 **Register Summary**.

## 43.7 Programming Procedures

### 43.7.1 Data Receiving Operation Process

This section introduces the programming procedure for receiving data in the RX unit. Perform the following procedure to receive parallel data from IO pins connected to external devices to be stored in the internal memory. For detailed description of the clock and reset operation restrictions in the RX unit, refer to Section 43.5.2.

1. Reset the RX unit. For specific reset scenarios and sequences, refer to Section 43.5.2.
2. Set `PARL_IO_RX_FIFO_WOVF_INT_CLR` and `PARL_IO_RX_FIFO_WOVF_INT_ENA`.
3. Select the RXD IO pins. If a PAD clock is used, the clock IO pin also needs to be configured.
4. Select the clock source and divide the clock by configuring PCR registers.
5. Turn off the clock of RX Core clock domain.
```