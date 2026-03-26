

```markdown
HP_SYS_CLKRST_UARTn_SCLK_DIV_NUMERATOR.

* Configure the baud rate for transmission via UART_CLKDIV and UART_CLKDIV_FRAG.
* Configure data length via UART_BIT_NUM.
* Configure odd or even parity check via UART_PARITY_EN and UART_PARITY.
* Optional steps depending on application ...
* Synchronize the configured values to the Core Clock domain by writing 1 to UART_REG_UPDATE.

### 42.5.2.3 Enabling UARTn

To enable UARTn transmitter:

* Configure TX FIFO's empty threshold via UART_TXFIFO_EMPTY_THRHDD.
* Disable UART_TXFIFO_EMPTY_INT interrupt by clearing UART_TXFIFO_EMPTY_INT_ENA.
* Write data to be sent to UART_RXFIFO_RD_BYTE.
* Clear UART_TXFIFO_EMPTY_INT interrupt by setting UART_TXFIFO_EMPTY_INT_CLR.
* Enable UART_TXFIFO_EMPTY_INT interrupt by setting UART_TXFIFO_EMPTY_INT_ENA.
* Check UART_TXFIFO_EMPTY_INT_ST and wait for the completion of data transmission.

To enable UARTn receiver:

* Configure RX FIFO's full threshold via UART_RXFIFO_FULL_THRHDD.
* Enable UART_RXFIFO_FULL_INT interrupt by setting UART_RXFIFO_FULL_INT_ENA.
* Check UART_RXFIFO_FULL_INT_ST and wait until the RX FIFO is full.
* Read data from RX FIFO via UART_RXFIFO_RD_BYTE, and obtain the number of bytes received in RX FIFO via UART_RXFIFO_CNT.
```