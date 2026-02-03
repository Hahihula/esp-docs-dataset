**Chapter Title:**
Chapter 26 UART Controller (UART)

**Body Text with List of Interrupts and Descriptions for UART:**

- **UART_RXFIFO_TOUT_INT:** Triggered when the receiver takes more time than UART_RX_TOUT_THRD to receive one byte.
- **UART_BRK_DET_INT:** Triggered when the receiver detects a NULL character (i.e., logic 0 for one NULL character transmission) after stop bits.
- **UART_CTS_CHG_INT:** Triggered when the receiver detects an edge change on CTSn signals.
- **UART_DSR_CHG_INT:** Triggered when the receiver detects an edge change on DSRn signals.
- **UART_RXFIFO_OVF_INT:** Triggered when the receiver receives more data than the capacity of the RX FIFO.
- **UART_FRM_ERR_INT:** Triggered when the receiver detects a data frame error.
- **UART_PARITY_ERR_INT:** Triggered when the receiver detects a parity error.
- **UART_TXFIFO_EMPTY_INT:** Triggered when the TX FIFO stores less data than what UART_TXFIFO_EMPTY_THRD specifies.
- **UART_RXFIFO_FULL_INT:** Triggered when the receiver receives more data than what UART_RXFIFO_FULL_THRD specifies.
- **UART_WAKEUP_INT:** Triggered when UART is woken up.

**Subtitle:**
26.4.13 UHCI Interrupts

**Body Text with List of Interrupts and Descriptions for UHCI:**

- **UHCI_APP_CTRL1_INT:** Triggered when software sets UHCI_APP_CTRL1_INT_RAW.
- **UHCI_APP_CTRL0_INT:** Triggered when software sets UHCI_APP_CTRL0_INT_RAW.
- **UHCI_OUTLINK_EOF_ERR_INT:** Triggered when an EOF error is detected in a transmit descriptor.
- **UHCI_SEND_A_REG_Q_INT:** Triggered when UHCI has sent a series of short packets using always_send.
- **UHCI_SEND_S_REG_Q_INT:** Triggered when UHCI has sent a series of short packets using single_send.
- **UHCI_TX_HUNG_INT:** Triggered when UHCI takes too long to read RAM using a GDMA transmit channel.
- **UHCI_RX_HUNG_INT:** Triggered when UHCI takes too long to receive data using a GDMA receive channel.

**Footer:**
Espressif Systems
937 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback