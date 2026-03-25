

```markdown
## 38.5.12 Bit Reversal in One Byte

The sequence of data within one byte can be reversed when data bus width is 1/2/4-bit. Taking the RX unit as an example, when the configured bus width is 2 bits, the data needs to be packed into one byte before being written into the RX FIFO.

Presume that the original bit sequence is:

```markdown
{{ b_0, b_1 }, { b_2, b_3 }, { b_4, b_5 }, { b_6, b_7 }}
```

If the bit reversal is enabled, the sequence will be reordered to:

```markdown
{{ b_6, b_7 }, { b_4, b_5 }, { b_2, b_3 }, { b_0, b_1 }}
```

## 38.6 Programming Procedures

### 38.6.1 Data Receiving Operation Process

This section introduces the programming procedure for receiving data through RX unit. To receive parallel data from IO pins that are connected to external devices and store the data in the internal memory, perform the following procedure. For a detailed description of the clock and reset operation restrictions in the RX unit, refer to Section 38.5.2.

1. Reset the RX unit. For specific reset scenarios and sequences, refer to Section 38.5.2.
2. Set `PARL_IO_RX_FIFO_WOVF_INT_CLR` and `PARL_IO_RX_FIFO_WOVF_INT_ENA`.
3. Select the RXD IO pins. If a PAD clock is used, the clock IO pin also needs to be configured.
4. Select the clock source and divide the clock by configuring PCR registers.
5. Turn off the clock of RX Core clock domain.
6. Select the receive mode and enable functions required as described in Sections 38.3 and 38.5.
7. Configure GDMA inlink list.
8. Set `PARL_IO_RX_REG_UPDATE` to synchronize the register signals.
9. Set `PARL_IO_RX_START`.
10. Turn on the clock of RX Core clock domain.
11. Operate the external device to start sending data.
12. Poll the GDMA SUC EOF interrupt.
13. Clear the GDMA SUC EOF interrupt.
14. Turn off the clock of RX Core clock domain.
15. Clear `PARL_IO_RX_START`.

### 38.6.2 Data Transmitting Operation Process

This section introduces the programming procedure for transmitting data through TX unit. To transmit parallel data from internal memory to the IO pins that are connected to external devices, perform the following
```