**Title:**
Chapter 26 UART Controller (UART)

**Subtitle:**
26.4.11 GDMA Mode

**Body Text:**

All three UART controllers on ESP32-S3 share one TX/RX GDMA (general direct memory access) channel via UHCI. In GDMA mode, UART controllers support the decoding and encoding of HCI data packets. The UHCI_UARTn_CE field determines which UART controller occupies the GDMA TX/RX channel.

**Figure:**
- Caption: Figure 26.4-11. Data Transfer in GDMA Mode
- Description:
  - Diagram showing components labeled as "UHCI," "Encoder," "Decoder," and connections to "MUX" with labels for "UART0," "UART1," etc.
  
**Additional Text under the figure:**
Figure 26.4-11 shows how data are transferred using GDMA. Before GDMA receives data, software prepares an inlink (i.e., a linked list of receive descriptors). For details, see Chapter 3 GDMA Controller (GDMA).
- GDMA_INLINK_ADDR_CHn points to the first receive descriptor in the inlink.
- After GDMA_INLINK_START_CHn is set, UHCI passes data that UART has received to the decoder. The decoded data are then stored into the RAM pointed by the inlink under the control of GDMA.

Before GDMA sends data, software prepares an outlink and data to be sent. GDMA_OUTLINK_ADDR_CHn points to the first transmit descriptor in the outlink. After GDMA_OUTLINK_START_CHn is set, GDMA reads data from the RAM pointed by outlink. The data are then encoded by the encoder, and sent sequentially by the UART transmitter.

HCI data packets have separators at the beginning and end, with data bits in the middle (separators + data bits + separators). The encoder inserts separators in front of and after data bits, and replaces data bits identical to separators with special characters (i.e., escape characters). The decoder removes separators in front of and after data bits, and replaces escape characters with separators. There can be more than one continuous separator at the beginning and end of a data packet. The separator is configured by UHCI_SEPER_CHAR, OxCO by default. The escape characters are configured by UHCI_ESC_SEQO_CHA0 (OxDB by default) and UHCI_ESC_SEQO_CHA1 (OxDD by default). When all data have been sent, a GDMA_OUT_TOTAL_EOF_CHn_INT interrupt is generated. When all data have been received, a GDMA_IN_SUC_EOF_CHn_INT is generated.

**Subtitle:**
26.4.12 UART Interrupts

**Body Text under the subtitle:**

- UART_AT_CMD_CHAR_DET_INT: Triggered when the receiver detects an AT_CMD character.
- UART_RS485_CLASH_INT: Triggered when a collision is detected between the transmitter and the receiver in RS485 mode.
- UART_RS485_FRM_ERR_IN: Triggered when an error is detected in the data frame sent by the transmitter in RS485 mode.

**Footer Information:**
Espressif Systems
936
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback