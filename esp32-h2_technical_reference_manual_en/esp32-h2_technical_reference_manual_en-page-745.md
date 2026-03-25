

```markdown
Register 28.38. UHCI_CONF0_REG (0x0000)
```

Continued from the previous page...

**UHCI_LEN_EOF_EN** Configures when the UHCI decoder stops receiving data.

- 0: Stops after receiving 0xC0
- 1: Stops when the number of received data bytes reach the specified value. When `UHCI_HEAD_EN` is 1, the specified value is the data length indicated by the UHCI packet header; when `UHCI_HEAD_EN` is 0, the specified value is the configured value.
(R/W)

**UHCI_ENCODE_CRC_EN** Configures whether or not to enable data integrity check by appending a 16 bit CCITT-CRC to the end of the data.

- 0: Disable
- 1: Enable
(R/W)

**UHCI_CLK_EN** Configures clock gating.

- 0: Support clock only when the application writes registers.
- 1: Always force the clock on for registers.
(R/W)

**UHCI_UART_RX_BRK_EOF_EN** Configures whether or not to stop UHCI from receiving data after UART has received a NULL frame.

- 0: Not stop
- 1: Stop
(R/W)
```