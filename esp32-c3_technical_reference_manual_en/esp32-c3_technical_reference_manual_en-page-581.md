

```markdown
Register 26.9. UART_CONF0_REG (0x0020)

Continued from the previous page...

UART_TXD_INV    Set this bit to invert the level value of UART TXD signal. (R/W)
UART_RTS_INV    Set this bit to invert the level value of UART RTS signal. (R/W)
UART_DTR_INV    Set this bit to invert the level value of UART DTR signal. (R/W)
UART_CLK_EN     1: Force clock on for register; 0: Support clock only when application writes registers. (R/W)
UART_ERR_WR_MASK 1: The receiver stops storing data into FIFO when data is wrong; 0: The receiver stores the data even if the received data is wrong. (R/W)
UART_AUTBAUD_EN This is the enable bit for baud rate detection. (R/W)
UART_MEM_CLK_EN The signal to enable UART RAM clock gating. (R/W)

Register 26.10. UART_CONF1_REG (0x0024)


| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0x60|      |      |      |      |      |      |      |      | Reset|      |      |      |      |      |      |      |
```

UART_RXFIFO_FULL_THRD An UART_RXFIFO_FULL_INT interrupt is generated when the receiver receives more data than the value of this field. (R/W)

UART_TXFIFO_EMPTY_THRD An UART_TXFIFO_EMPTY_INT interrupt is generated when the number of data bytes in TX FIFO is less than the value of this field. (R/W)

UART_DIS_RX_DAT_OVF Disable UART RX data overflow detection. (R/W)

UART_RX_TOUT_FLOW_DIS Set this bit to stop accumulating idle_cnt when hardware flow control works. (R/W)

UART_RX_FLOW_EN This is the flow enable bit for UART receiver. (R/W)

UART_RX_TOUT_EN This is the enable bit for UART receiver's timeout function. (R/W)
```