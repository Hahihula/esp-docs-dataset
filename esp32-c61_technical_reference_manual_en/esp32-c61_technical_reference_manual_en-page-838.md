

```markdown
HW_Flow_Ctrl controls rxd_in and txd_out data flows by standard UART RTS and CTS flow control signals (rtsn_out and ctsn_in). SW_Flow_Ctrl controls data flows by adding special characters to outgoing data and detecting special characters in incoming data. When a UART controller is in Light-sleep mode (see Chapter 11 Low-Power Management for more details), a wake_up signal can be generated in four ways and sent to PMU, which then wakes up the ESP32-C61 chip. For more information about wakeup, please refer to Section 25.4.8.

## 25.4 Functional Description

### 25.4.1 Clock and Reset

UART controllers are asynchronous. Their register configuration module works in the APB_CLK domain. TX FIFO and RX FIFO work across the AHB_CLK and UART_FCLK domains. The UART RAM control unit works in the UART_FCLK domain. The UART transmission and reception control module works in the UART_SCLK domain, i.e., UART Core's clock domain.

When the frequency of the UART_SCLK is higher than the frequency needed to generate the baud rate, the UART Core can be clocked at a lower frequency by the divider, in order to reduce power consumption. Usually, the UART Core's clock frequency is lower than the APB_CLK's frequency, and can be divided by the largest divisor when higher than the frequency needed to generate the baud rate. The frequency of the UART Core's clock can also be at most twice higher than the APB_CLK. The clock for the UART transmitter and the UART receiver can be controlled independently. To enable the clock for the UART transmitter, `UART_TX_SCLK_EN` shall be set; to enable the clock for the UART receiver, `UART_RX_SCLK_EN` shall be set.

To ensure that the configured register values are synchronized from APB_CLK domain to the UART_SCLK domain, please follow the procedures in Section25.6.

To reset the whole UART, please:

* Enable the UART Core's clock by setting `PCR_UARTn_CLK_EN` to 1.
* Write 1 to `PCR_UARTn_RST_EN`.
* Clear `PCR_UARTn_RST_EN` to 0.

### 25.4.2 UART FIFO

The transmitter and the receiver on the UART controller each use a 128 x 8-bit RAM, and access their respective RAM through a separate 4 x 8-bit asynchronous FIFO interface. The RAM and asynchronous FIFO interface for the transmitter and the receiver are independent and cannot be shared.

UART Tx_FIFO is reset by setting `UART_TXFIFO_RST`. UART Rx_FIFO is reset by setting `UART_RXFIFO_RST`.

Data to be sent is written to TX FIFO via the APB bus, read automatically, and converted from a frame into a bitstream by hardware Tx_FSM. Data received is converted from a bitstream into a frame by hardware Rx_FSM, written into RX FIFO, and then stored into RAM via the APB bus.

The empty signal threshold for Tx_FIFO is configured by setting `UART_TXFIFO_EMPTY_THRD`. When data stored in Tx_FIFO is less than `UART_TXFIFO_EMPTY_THRD`, a UART_TXFIFO_EMPTY_INT interrupt is generated. The full signal threshold for Rx_FIFO is configured by setting `UART_RXFIFO_FULL_THRD`.
```