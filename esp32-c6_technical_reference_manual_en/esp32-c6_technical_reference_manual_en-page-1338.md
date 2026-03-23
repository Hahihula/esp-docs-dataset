

```markdown
The bus idle value is 0x0 by default, and its maximum configurable value is 0xFFFF. Note that the configured idle value should not conflict with other enabled functions. For example, when the MSB of TXD is used as the valid signal, users should avoid configuring the MSB of the idle value as 1.

## 38.5.9 Data Transfer in a Single Frame

The RX unit and the TX unit are transferred in the unit of bytes, i.e., a single frame transfers 1 byte of data at least.

When the RX unit generates GDMA EOF signals through byte length, the maximum length of the single-frame transmission is (2^16 – 1) bytes. When the RX unit generates GDMA EOF signals through the enable signal from an external device, there is no limit to the amount of bytes of the single-frame transmission.

The TX unit only generates GDMA EOF signals through byte length, so the maximum length of a single frame transmission is (2^16 – 1) bytes.

When the configured data bus width is 16 bit, the byte length must be configured as a multiple of 2 bytes.

Normally, PARLIO can perform full-duplex transfer. But when in 16-bit bus width mode, PARAIO can only perform half-duplex transfer due to the limitation of the IO numbers.

## 38.5.10 Bit Reordering in One Byte

The sequence of data within one byte can be reversed. Taking the RX unit as an example, when the configured bus width is 2 bit, the data needs to be packed into one byte before being written into the RX FIFO.

Presume that the original bit sequence is:

```markdown
{{b_0, b_1}, {b_2, b_3}, {b_4, b_5}, {b_6, b_7}}
```

If the bit reordering function is enabled, the sequence will be reordered to:

```markdown
{{b_6, b_7}, {b_4, b_5}, {b_2, b_3}, {b_0, b_1}}
```

## 38.6 Programming Procedures

### 38.6.1 Data Receiving Operation Process

This section introduces the programming procedure for receiving data in the RX unit. Perform the following procedure to receive parallel data from IO pins connected to external devices to be stored in the internal memory. For detailed description of the clock and reset operation restrictions in the RX unit, refer to Section 38.5.2.

1. Reset the RX unit. For specific reset scenarios and sequences, refer to Section 38.5.2.
2. Set `PARL_IO_RX_FIFO_WFULL_INT_CLR` and `PARL_IO_RX_FIFO_WFULL_INT_ENA`.
3. Select the RXD IO pins. If a PAD clock is used, the clock IO pin also needs to be configured.
4. Select the clock source and divide the clock by configuring PCR registers.
5. Turn off the clock of RX Core clock domain.
```