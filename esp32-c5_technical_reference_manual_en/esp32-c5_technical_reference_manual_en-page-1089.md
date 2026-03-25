

```markdown
## 32.8.3 UHCI Registers

The addresses in this section are relative to UHCI base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 32.70. UHCI_CONFO_REG (0x0000)

| Bit | Name                        | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                  |                                                                             |
| 30  | UHCI_UART_RX_RST            | Write 1 and then write 0 to reset the decoder state machine. (R/W)          |
| 29  | UHCI_RX_RST                 | Write 1 and then write 0 to reset the encoder state machine. (R/W)          |
| 28  | UHCI_UART_SEL               | Select one UART from UART 0 ~ 1 to connect with UHCI.<br>0: Select UART0<br>1: Select UART1<br>2 ~ 7: No effect, as no UART will connect with UHCI (R/W) |
| 27  | UHCI_UART1_CE               | Configures whether or not to connect UHCI with UART1.<br>0: Not connect<br>1: Connect (R/W) |
| 26  | UHCI_SEPER_EN               | Configures whether or not to separate the data frame with a special character.<br>0: Not separate<br>1: Separate (R/W) |
| 25  | UHCI_HEAD_EN                | Configures whether or not to encode the data packet with a formatting header.<br>0: Not use formatting header<br>1: Use formatting header (R/W) |

Continued on the next page...
```