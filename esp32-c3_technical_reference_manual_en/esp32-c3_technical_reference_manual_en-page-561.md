

```markdown
hardware. As a result, the transmitter sends an XON character configured by UART_XON_CHAR after the current byte in transmission.

## 26.4.10 GDMA Mode

The two UART controllers on ESP32-C3 share one TX/RX GDMA (general direct memory access) channel via UHCI. In GDMA mode, UART controllers support the decoding and encoding of HCI data packets. The `UHCI_UARTn_CE` field determines which UART controller occupies the GDMA TX/RX channel.

![Figure 26.4-11. Data Transfer in GDMA Mode](#)

**Figure 26.4-11. Data Transfer in GDMA Mode**

Figure 26.4-11 shows how data is transferred using GDMA. Before GDMA receives data, software prepares an inlink. `GDMA_INLINK_ADDR_CHn` points to the first receive descriptor in the inlink. After `GDMA_INLINK_START_CHn` is set, UHCI sends data that UART has received to the decoder. The decoded data is then stored into the RAM pointed by the inlink under the control of GDMA.

Before GDMA sends data, software prepares an outlink and data to be sent. `GDMA_OUTLINK_ADDR_CHn` points to the first transmit descriptor in the outlink. After `GDMA_OUTLINK_START_CHn` is set, GDMA reads data from the RAM pointed by outlink. The data is then encoded by the encoder, and sent sequentially by the UART transmitter.

HCI data packets have separators at the beginning and the end, with data bits in the middle (separators + data bits + separators). The encoder inserts separators in front of and after data bits, and replaces data bits identical to separators with special characters. The decoder removes separators in front of and after data bits, and replaces special characters with separators. There can be more than one continuous separator at the beginning and the end of a data packet. The separator is configured by `UHCI_SEPER_CHAR`, 0xC0 by default. The special character is configured by `UHCI_ESC_SEQO_CHAR0` (0xDB by default) and `UHCI_ESC_SEQO_CHAR1` (0xDD by default). When all data has been sent, a `GDMA_OUT_TOTAL_EOF_CHn_INT` interrupt is generated. When all data has been received, a `GDMA_IN_SUC_EOF_CHn_INT` is generated.

## 26.4.11 UART Interrupts

*   `UART_AT_CMD_CHAR_DET_INT`: Triggered when the receiver detects an AT_CMD character.
*   `UART_RS485_CLASH_INT`: Triggered when a collision is detected between the transmitter and the receiver in RS485 mode.
*   `UART_RS485_FRM_ERR_INT`: Triggered when an error is detected in the data frame sent by the transmitter in RS485 mode.
```