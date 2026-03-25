

```markdown
Register 25.19. UART_RS485_CONF_SYNC_REG (0x004C)

UART_RS485_EN Configures whether or not to enable RS485 mode.
O: Disable
1: Enable
(R/W)

UART_DLO_EN Configures whether or not to add a turnaround delay of 1 bit before the start bit.
O: Not add
1: Add
(R/W)

UART_DL1_EN Configures whether or not to add a turnaround delay of 1 bit after the stop bit.
O: Not add
1: Add
(R/W)

UART_RS485TX_RX_EN Configures whether or not to enable the receiver for data reception when the transmitter is transmitting data in RS485 mode.
O: Disable
1: Enable
(R/W)

UART_RS485RXBY_TX_EN Configures whether to enable the RS485 transmitter for data transmission when the RS485 receiver is busy.
O: Disable
1: Enable
(R/W)

UART_RS485_RX_DLY_NUM Configures the delay of internal data signals in the receiver.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)

UART_RS485_TX_DLY_NUM Configures the delay of internal data signals in the transmitter.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```