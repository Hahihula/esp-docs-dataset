

```markdown
Figure 27.4-10 shows how data is transferred using GDMA. Before GDMA receives data, software prepares an inlink. GDMA_INLINK_ADDR_CHn points to the first receive descriptor in the inlink. After GDMA_INLINK_START_CHn is set, UHCI sends data that UART has received to the decoder. The decoded data is then stored into the RAM pointed by the inlink under the control of GDMA.

Before GDMA sends data, software prepares an outlink and data to be sent. GDMA_OUTLINK_ADDR_CHn points to the first transmit descriptor in the outlink. After GDMA_OUTLINK_START_CHn is set, GDMA reads data from the RAM pointed by outlink. The data is then encoded by the encoder, and sent sequentially by the UART transmitter.

HCI data packets have separators at the beginning and the end, with data bits in the middle (separators + data bits + separators). The encoder inserts separators in front of and after data bits, and replaces data bits identical to separators with special characters. The decoder removes separators in front of and after data bits, and replaces special characters with separators. There can be more than one continuous separator at the beginning and the end of a data packet. The separator is configured by UHCI_SEPER_CHAR, 0xC0 by default. The special character is configured by UHCI_ESC_SEQO_CHAR0 (0xDB by default) and UHCI_ESC_SEQO_CHAR1 (0xDD by default). When all data has been sent, a GDMA_OUT_TOTAL_EOF_CHn_INT interrupt is generated. When all data has been received, a GDMA_IN_SUC_EOF_CHn_INT is generated.
```