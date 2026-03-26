

```markdown
Register 42.69. UHCI_CONFO_REG (0x0000)

Continued from the previous page...

UHCI_CRC_REC_EN Configures whether or not to enable the reception of the 16-bit CRC.
O: Disable
1: Enable
(R/W)

UHCI_UART_IDLE_EOF_EN Configures whether or not to stop receiving data when UART is idle.
O: Not stop
1: Stop
(R/W)

UHCI_LEN_EOF_EN Configures when the UHCI decoder stops receiving data.
O: Stops after receiving 0xCO
1: Stops when the number of received data bytes reach the specified value. When UHCI_HEAD_EN is 1, the specified value is the data length indicated by the UHCI packet header; when UHCI_HEAD_EN is O, the specified value is the configured value.
(R/W)

UHCI_ENCODE_CRC_EN Configures whether or not to enable data integrity check by appending a 16 bit CCITT-CRC to the end of the data.
O: Disable
1: Enable
(R/W)

UHCI_CLK_EN Configures clock gating.
O: Support clock only when the application writes registers.
1: Always force the clock on for registers.
(R/W)

UHCI_UART_RX_BRK_EOF_EN Configures whether or not to stop UHCI from receiving data after UART has received a NULL frame.
O: Not stop
1: Stop
(R/W)
```