

```markdown
## 42.7.3 UHCI Registers

The addresses in this section are relative to UHCI base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 42.69. UHCI_CONFO_REG (0x0000)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)               |                                                                             |
| 30  |                          |                                                                             |
| ... |                          |                                                                             |
| 2   | UHCI_UART_SEL            | Select UART to connect with UHCI                                           |
| 1   | UHCI_RX_RST              | Write 1 and then write 0 to reset the decoder state machine. (R/W)          |
| 0   | UHCI_TX_RST              | Write 1 and then write 0 to reset the encoder state machine. (R/W)          |

UHCI_UART_CE Select one UART from UART 0 ~ 4 to connect with UHCI.
- 0: Select UART0
- 1: Select UART1
- 2: Select UART2
- 3: Select UART3
- 4: Select UART4
- 5 ~ 7: No effect, as no UART will connect with UHCI (R/W)

UHCI_UART1_CE Configures whether or not to connect UHCI with UART1.
- 0: Not connect
- 1: Connect (R/W)

UHCI_SEPER_EN Configures whether or not to separate the data frame with a special character.
- 0: Not separate
- 1: Separate (R/W)

UHCI_HEAD_EN Configures whether or not to encode the data packet with a formatting header.
- 0: Not use formatting header
- 1: Use formatting header (R/W)
```