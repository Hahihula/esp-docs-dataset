

```markdown
Register 28.9. UART_CONFO_SYNC_REG (0x0020)

Continued from the previous page...

UART_IRDA_WCTL Configures the 11th bit of the IrDA transmitter.
O: This bit is 0.
1: This bit is the same as the 10th bit.
(R/W)

UART_IRDA_TX_INV Configures whether or not to invert the level of the IrDA transmitter.
O: Not invert
1: Invert
(R/W)

UART_IRDA_RX_INV Configures whether or not to invert the level of the IrDA receiver.
O: Not invert
1: Invert
(R/W)

UART_LOOPBACK Configures whether or not to enable UART loopback test.
O: Disable
1: Enable
(R/W)

UART_TX_FLOW_EN Configures whether or not to enable flow control for the transmitter.
O: Disable
1: Enable
(R/W)

UART_IRDA_EN Configures whether or not to enable IrDA protocol.
O: Disable
1: Enable
(R/W)

UART_RXD_INV Configures whether or not to invert the level of UART RXD signal.
O: Not invert
1: Invert
(R/W)

UART_TXD_INV Configures whether or not to invert the level of UART TXD signal.
O: Not invert
1: Invert
(R/W)

UART_DIS_RX_DAT_OVF Configures whether or not to disable data overflow detection for the UART receiver.
O: Enable
1: Disable
(R/W)
```