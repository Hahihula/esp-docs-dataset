

```markdown
Register 27.70. UHCI_CONF0_REG (0x0000)
```

Continued from the previous page...

UHCI_ENCODE_CRC_EN Configures whether or not to enable data integrity check by appending a 16 bit CCITT-CRC to the end of the data.
- O: Disable
- 1: Enable
(R/W)

UHCI_CLK_EN Configures clock gating.
- O: Support clock only when the application writes registers.
- 1: Always force the clock on for registers.
(R/W)

UHCI_UART_RX_BRK_EOF_EN Configures whether or not to stop UHCI from receiving data after UART has received a NULL frame.
- O: Not stop
- 1: Stop
(R/W)
```