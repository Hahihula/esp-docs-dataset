

```markdown
Register 26.34. UHCI_CONF0_REG (0x0000)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 13  | UHCI_UART_TX_RST Write 1, then write 0 to this bit to reset decode state machine. (R/W) |
| 12  | UHCI_RX_RST Write 1, then write 0 to this bit to reset encode state machine. (R/W) |
| 11  | UHCI_UARTO_CE Set this bit to link up UHCI and UARTO. (R/W) |
| 10  | UHCI_UART1_CE Set this bit to link up UHCI and UART1. (R/W) |
| 9   | UHCI_SEPER_EN Set this bit to separate the data frame using a special character. (R/W) |
| 8   | UHCI_HEAD_EN Set this bit to encode the data packet with a formatting header. (R/W) |
| 7   | UHCI_CRC_REC_EN Set this bit to enable UHCI to receive the 16 bit CRC. (R/W) |
| 6   | UHCI_UART_IDLE_EOF_EN If this bit is set to 1, UHCI will end the payload receiving process when UART has been in idle state. (R/W) |
| 5   | UHCI_LEN_EOF_EN If this bit is set to 1, UHCI decoder stops receiving payload data when the number of received data bytes has reached the specified value. The value is payload length indicated by UHCI packet header when UHCI_HEAD_EN is 1 or the value is configuration value when UHCI_HEAD_EN is 0. If this bit is set to 0, UHCI decoder stops receiving payload data when OxC0 has been received. (R/W) |
| 4   | UHCI_ENCODE_CRC_EN Set this bit to enable data integrity check by appending a 16 bit CCITT-CRC to end of the payload. (R/W) |
| 3   | UHCI_CLK_EN 1: Force clock on for register; 0: Support clock only when application writes registers. (R/W) |
| 2   | UHCI_UART_RX_BRK_EOF_EN If this bit is set to 1, UHCI will end payload receive process when NULL frame is received by UART. (R/W) |
| 1   | Reset |
| 0   | Reset |
```