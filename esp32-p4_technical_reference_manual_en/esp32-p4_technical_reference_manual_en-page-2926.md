

```markdown
Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 58.9 Register Summary.

## 58.7 Programming Procedures

### 58.7.1 Data Receiving Operation Process

This section introduces the programming procedure for receiving data through RX unit. To receive parallel data from IO pins that are connected to external devices and store the data in the internal memory, perform the following procedure. For a detailed description of the clock and reset operation restrictions in the RX unit, refer to Section 58.5.2.

1. Reset the RX unit. For specific reset scenarios and sequences, refer to Section 58.5.2.
2. Set `PARL_IO_RX_FIFO_WOVF_INT_CLR` and `PARL_IO_RX_FIFO_WOVF_INT_ENA`.
3. Select the RXD IO pins. If a PAD clock is used, the clock IO pin also needs to be configured.
4. Select the clock source and divide the clock by configuring clock registers.
5. Turn off the clock of RX Core clock domain.
6. Select the receive mode and enable functions required as described in Sections 58.3 and 58.5.
7. Configure GDMA inlink list.
8. Set `PARL_IO_RX_REG_UPDATE` to synchronize the register signals.
9. Set `PARL_IO_RX_START`.
10. Turn on the clock of RX Core clock domain.
11. Operate the external device to start sending data.
12. Poll the GDMA SUC EOF interrupt.
13. Clear the GDMA SUC EOF interrupt.
14. Turn off the clock of RX Core clock domain.
15. Clear `PARL_IO_RX_START`.

### 58.7.2 Data Transmitting Operation Process

This section introduces the programming procedure for transmitting data through TX unit. To transmit parallel data from internal memory to the IO pins that are connected to external devices, perform the following procedure. For detailed description of the clock and reset operation restrictions for the TX unit, refer to Section 58.5.2.

1. Reset the TX unit. For specific reset scenarios and sequences, refer to Section 58.5.2.
```