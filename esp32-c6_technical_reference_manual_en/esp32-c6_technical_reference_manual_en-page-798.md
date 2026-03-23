

```markdown
Register 27.70. UHCI_CONF0_REG (0x0000)

31                         13 12 11 10 9 8 7 6 5 4 3 2 1 0
+------------------------------------------------------------------------------+
| RESERVED | UHCI_UART_TX_RST | UHCI_RX_RST | UHCI_UART_CE | UHCI_UART1_CE | UHCI_SEPER_EN | UHCI_HEAD_EN | UHCI_CRC_REC_EN | UHCI_UART_IDLE_EOF_EN | UHCI_LEN_EOF_EN |
+------------------------------------------------------------------------------+

UHCI_TX_RST Write 1 and then write 0 to reset the decoder state machine. (R/W)

UHCI_RX_RST Write 1 and then write 0 to reset the encoder state machine. (R/W)

UHCI_UART_CE Configures whether or not to connect UHCI with UART0.
    0: Not connect
    1: Connect
    (R/W)

UHCI_UART1_CE Configures whether or not to connect UHCI with UART1.
    0: Not connect
    1: Connect
    (R/W)

UHCI_SEPER_EN Configures whether or not to separate the data frame with a special character.
    0: Not separate
    1: Separate
    (R/W)

UHCI_HEAD_EN Configures whether or not to encode the data packet with a formatting header.
    0: Not use formatting header
    1: Use formatting header
    (R/W)

UHCI_CRC_REC_EN Configures whether or not to enable the reception of the 16-bit CRC.
    0: Disable
    1: Enable
    (R/W)

UHCI_UART_IDLE_EOF_EN Configures whether or not to stop receiving data when UART is idle.
    0: Not stop
    1: Stop
    (R/W)

UHCI_LEN_EOF_EN Configures when the UHCI decoder stops receiving data.
    0: Stops after receiving 0xCO
    1: Stops when the number of received data bytes reach the specified value. When UHCI_HEAD_EN is 1, the specified value is the data length indicated by the UHCI packet header; when UHCI_HEAD_EN is 0, the specified value is the configured value.
    (R/W)
```