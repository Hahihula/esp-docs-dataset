

```markdown
Chapter 28 UART Controller (UART)

GoBack

28.5.2.3 Enabling UARTn

To enable UARTn transmitter:

* Configure TX FIFO's empty threshold via `UART_TXFIFO_EMPTY_THRHDD`.
* Disable UART_TXFIFO_EMPTY_INT interrupt by clearing `UART_TXFIFO_EMPTY_INT_ENA`.
* Write data to be sent to `UART_RXFIFO_RD_BYTE`.
* Clear UART_TXFIFO_EMPTY_INT interrupt by setting `UART_TXFIFO_EMPTY_INT_CLR`.
* Enable UART_TXFIFO_EMPTY_INT interrupt by setting `UART_TXFIFO_EMPTY_INT_ENA`.
* Check `UART_TXFIFO_EMPTY_INT_ST` and wait for the completion of data transmission.

To enable UARTn receiver:

* Configure RX FIFO's full threshold via `UART_RXFIFO_FULL_THRHDD`.
* Enable UART_RXFIFO_FULL_INT interrupt by setting `UART_RXFIFO_FULL_INT_ENA`.
* Check `UART_RXFIFO_FULL_INT_ST` and wait until the RX FIFO is full.
* Read data from RX FIFO via `UART_RXFIFO_RD_BYTE`, and obtain the number of bytes received in RX FIFO via `UART_RXFIFO_CNT`.

Espressif Systems
717
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```