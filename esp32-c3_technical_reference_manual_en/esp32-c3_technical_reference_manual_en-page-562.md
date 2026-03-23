

```markdown
UART_RS485_PARITY_ERR_INT: Triggered when an error is detected in the parity bit sent by the transmitter in RS485 mode.
UART_TX_DONE_INT: Triggered when all data in the transmitter's TX FIFO has been sent.
UART_TX_BRK_IDLE_DONE_INT: Triggered when the transmitter stays idle for the minimum interval (threshold) after sending the last data bit.
UART_TX_BRK_DONE_INT: Triggered when the transmitter has sent all NULL characters after all data in TX FIFO had been sent.
UART_GLITCH_DET_INT: Triggered when the receiver detects a glitch in the middle of the start bit.
UART_SW_XOFF_INT: Triggered when UART_SW_FLOW_CON_EN is set and the receiver receives a XOFF character.
UART_SW_XON_INT: Triggered when UART_SW_FLOW_CON_EN is set and the receiver receives a XON character.
UART_RXFIFO_TOUT_INT: Triggered when the receiver takes more time than UART_RX_TOUT_THRD to receive one byte.
UART_BRK_DET_INT: Triggered when the receiver detects a NULL character (i.e. logic 0 for one NULL character transmission) after stop bits.
UART_CTS_CHG_INT: Triggered when the receiver detects an edge change of CTSn signals.
UART_DSR_CHG_INT: Triggered when the receiver detects an edge change of DSRn signals.
UART_RXFIFO_OVF_INT: Triggered when the receiver receives more data than the capacity of RX FIFO.
UART_FRM_ERR_INT: Triggered when the receiver detects a data frame error.
UART_PARITY_ERR_INT: Triggered when the receiver detects a parity error.
UART_TXFIFO_EMPTY_INT: Triggered when TX FIFO stores less data than what UART_TXFIFO_EMPTY_THRD specifies.
UART_RXFIFO_FULL_INT: Triggered when the receiver receives more data than what UART_RXFIFO_FULL_THRD specifies.
UART_WAKEUP_INT: Triggered when UART is woken up.

26.4.12 UHCI Interrupts

UHCI_APP_CTRL1_INT: Triggered when software sets UHCI_APP_CTRL1_INT_RAW.
UHCI_APP_CTRL0_INT: Triggered when software sets UHCI_APP_CTRL0_INT_RAW.
UHCI_OUTLINK_EOF_ERR_INT: Triggered when an EOF error is detected in a transmit descriptor.
UHCI_SEND_A_REG_Q_INT: Triggered when UHCI has sent a series of short packets using always_send.
UHCI_SEND_S_REG_Q_INT: Triggered when UHCI has sent a series of short packets using single_send.
UHCI_TX_HUNG_INT: Triggered when UHCI takes too long to read RAM using a GDMA transmit channel.
UHCI_RX_HUNG_INT: Triggered when UHCI takes too long to receive data using a GDMA receive channel.
UHCI_TX_START_INT: Triggered when GDMA detects a separator character.
```