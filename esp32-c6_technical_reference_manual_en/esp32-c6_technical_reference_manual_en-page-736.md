

```markdown
To reset the whole UART, please:
* Enable the UART Core’s clock by setting `PCR_UARTn_CLK_EN` to 1.
* Write 1 to `PCR_UARTn_RST_EN`.
* Clear `PCR_UARTn_RST_EN` to 0.

## 27.4.2 UART FIFO

The transmitter and the receiver on the UART controller each use a 128 x 8-bit RAM, and access their respective RAM through a separate 4 x 8-bit asynchronous FIFO interface. The RAM and asynchronous FIFO interface for the transmitter and the receiver are independent and cannot be shared.

UART0 Tx_FIFO and UART1 Tx_FIFO are reset by setting `UART_TXFIFO_RST`. UART0 Rx_FIFO and UART1 Rx_FIFO are reset by setting `UART_RXFIFO_RST`.

Data to be sent is written to TX FIFO via the APB bus or using GDMA, read automatically, and converted from a frame into a bitstream by hardware Tx FSM. Data received is converted from a bitstream into a frame by hardware Rx FSM, written into RX FIFO, and then stored into RAM via the APB bus or using GDMA. The two UART controllers share one GDMA channel.

The empty signal threshold for Tx_FIFO is configured by setting `UART_TXFIFO_EMPTY_THRD`. When data stored in Tx_FIFO is less than `UART_TXFIFO_EMPTY_THRD`, a `UART_TXFIFO_EMPTY_INT` interrupt is generated. The full signal threshold for Rx_FIFO is configured by setting `UART_RXFIFO_FULL_THRD`. When data stored in Rx_FIFO is greater than or equal to `UART_RXFIFO_FULL_THRD`, a `UART_RXFIFO_FULL_INT` interrupt is generated. In addition, when Rx_FIFO receives more data than its capacity, a `UART_RXFIFO_OVF_INT` interrupt is generated.

`UARTn` can access FIFO via register `UART_FIFO_REG`. Writing to `UART_RXFIFO_RD_BYTE` stores the data into the TX FIFO. As `UART_RXFIFO_RD_BYTE` is a read-only register field, the hardware does not actually perform a write operation on `UART_RXFIFO_RD_BYTE`; instead, upon detecting a write request to this field’s address, it passes the corresponding write data to the TX FIFO via a separate bypass. Reading `UART_RXFIFO_RD_BYTE` retrieves the data from the RX FIFO.
```