

```markdown
Chapter 42 UART Controller (UART)

Register 42.46. LP_UART_CONFO_SYNC_REG (0x0020)

LP_UART_PARITY   Configures the parity check mode.
O: Even parity
1: Odd parity
(R/W)

LP_UART_PARITY_EN Configures whether or not to enable LP UART parity check.
O: Disable
1: Enable
(R/W)

LP_UART_BIT_NUM   Configures the number of data bits.
O: 5 bits
1: 6 bits
2: 7 bits
3: 8 bits
(R/W)

LP_UART_STOP_BIT_NUM Configures the number of stop bits.
O: Invalid. No effect
1: 1 bit
2: 1.5 bits
3: 2 bits
(R/W)

LP_UART_TXD_BRK    Configures whether or not to send NULL characters when finishing data transmission.
O: Not send
1: Send
(R/W)

LP_UART_LOOPBACK   Configures whether or not to enable LP UART loopback test.
O: Disable
1: Enable
(R/W)

Continued on the next page...
```