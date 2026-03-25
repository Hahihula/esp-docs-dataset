

```markdown
## 28.4.2 UART FIFO

The transmitter and the receiver on the UART controller each use a 128 x 8-bit RAM, and access their respective RAM through a separate 4 x 8-bit asynchronous FIFO interface. The RAM and asynchronous FIFO interface for the transmitter and the receiver are independent and cannot be shared.

UART0 Tx_FIFO and UART1 Tx_FIFO are reset by setting `UART_TXFIFO_RST`. UART0 Rx_FIFO and UART1 Rx_FIFO are reset by setting `UART_RXFIFO_RST`.

Data to be sent is written to TX FIFO via the APB bus or using GDMA, read automatically, and converted from a frame into a bitstream by hardware Tx FSM. Data received is converted from a bitstream into a frame by hardware Rx FSM, written into RX FIFO, and then stored into RAM via the APB bus or using GDMA. The two UART controllers share one GDMA channel.

The empty signal threshold for Tx_FIFO is configured by setting `UART_TXFIFO_EMPTY_THRD`. When data stored in Tx_FIFO is less than `UART_TXFIFO_EMPTY_THRD`, a UART_TXFIFO_EMPTY_INT interrupt is generated. The full signal threshold for Rx_FIFO is configured by setting `UART_RXFIFO_FULL_THRD`. When data stored in Rx_FIFO is greater than or equal to `UART_RXFIFO_FULL_THRD`, a UART_RXFIFO_FULL_INT interrupt is generated. In addition, when Rx_FIFO receives more data than its capacity, a UART_RXFIFO_OVF_INT interrupt is generated.

`UARTn` can access FIFO via register `UART_FIFO_REG`. You can put data into TX FIFO by writing `UART_RXFIFO_RD_BYTE`, and get data in RX FIFO by reading `UART_RXFIFO_RD_BYTE`.

## 28.4.3 Baud Rate Generation and Detection

### 28.4.3.1 Baud Rate Generation

Before a UART controller sends or receives data, the baud rate should be configured by setting corresponding registers. The baud rate generator of a UART controller functions by dividing the input clock source. It can divide the clock source by a fractional amount. The divisor is configured by `UART_CLKDIV_SYNC_REG`: `UART_CLKDIV` for the integral part, and `UART_CLKDIV_FRAG` for the fractional part. When using the 80 MHz input clock, the UART controller supports a maximum baud rate of 5 Mbaud.

The divisor of the baud rate divider is equal to

```
UART_CLKDIV + UART_CLKDIV_FRAG / 16
```

meaning that the final baud rate is equal to

```
INPUT_FREQ / (UART_CLKDIV + UART_CLKDIV_FRAG / 16)
```

where `INPUT_FREQ` is the frequency of UART Core’s source clock. For example, if `UART_CLKDIV = 694` and `UART_CLKDIV_FRAG = 7`, then the divisor value is

```
694 + (7/16) = 694.4375
```

When `UART_CLKDIV_FRAG` is 0, the baud rate generator is an integer clock divider where an output pulse is generated every `UART_CLKDIV` input pulses.

When `UART_CLKDIV_FRAG` is not 0, the divider is fractional and the output baud rate clock pulses are not strictly uniform. As shown in Figure 28.4-1, for every 16 output pulses, the generator divides either
```