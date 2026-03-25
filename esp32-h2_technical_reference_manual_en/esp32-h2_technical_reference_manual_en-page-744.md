

```markdown
## 28.7.2 UHCI Registers

The addresses in this section are relative to UHCI base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 28.38. UHCI_CONF0_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 30  | UHCI_UART_RX_BRK_EOF_EN |
| 29  | UHCI_CLK_EN |
| 28  | UHCI_ENCODE_OFID_EN |
| 27  | UHCI_UART_IDLE_EOF_EN |
| 26  | UHCI_UART1_CIRC_EN |
| 25  | UHCI_UART1_CIRC_HEAD_EN |
| 24  | UHCI_SEPER_EN |
| 23  | (reserved) |
| 22  | UHCI_UART1_CE |
| 21  | UHCI_UART_RX_RST |
| 20  | UHCI_TX_RST |

- **UHCI_TX_RST**: Write 1 and then write 0 to reset the decoder state machine. (R/W)
- **UHCI_RX_RST**: Write 1 and then write 0 to reset the encoder state machine. (R/W)
- **UHCI_UART0_CE**: Configures whether or not to connect UHCI with UART0.
    - 0: Not connect
    - 1: Connect
    - (R/W)
- **UHCI_UART1_CE**: Configures whether or not to connect UHCI with UART1.
    - 0: Not connect
    - 1: Connect
    - (R/W)
- **UHCI_SEPER_EN**: Configures whether or not to separate the data frame with a special character.
    - 0: Not separate
    - 1: Separate
    - (R/W)
- **UHCI_HEAD_EN**: Configures whether or not to encode the data packet with a formatting header.
    - 0: Not use formatting header
    - 1: Use formatting header
    - (R/W)
- **UHCI_CRC_REC_EN**: Configures whether or not to enable the reception of the 16-bit CRC.
    - 0: Disable
    - 1: Enable
    - (R/W)
- **UHCI_UART_IDLE_EOF_EN**: Configures whether or not to stop receiving data when UART is idle.
    - 0: Not stop
    - 1: Stop
    - (R/W)

Continued on the next page...
```