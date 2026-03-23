

```markdown
Register 26.16. UART_IDLE_CONF_REG (0x0048)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)         |                                                                             |
| 20  | UART_TX_IDLE_NUM   | This field is used to configure the duration time between transfers, in the unit of bit time (the time it takes to transfer one bit). (R/W) |
| 19  |                    |                                                                             |
| 10  |                    |                                                                             |
| 9   |                    |                                                                             |
| 0   | UART_RX_IDLE_THRD  | A frame end signal is generated when the receiver takes more time to receive one byte data than the value of this field, in the unit of bit time (the time it takes to transfer one bit). (R/W) |

Register 26.17. UART_RS485_CONF_REG (0x004C)

| Bit | Field Name                         | Description                                                                 |
|-----|------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                         |                                                                             |
| 10  | UART_RS485_TX_DLY_NUM              | This field is used to delay the transmitter's internal data signal. (R/W)     |
| 9   | UART_RS485_RX_DLY_NUM              | This bit is used to delay the receiver's internal data signal. (R/W)          |
| 6   | UART_RS485_EN                      | Set this bit to choose RS485 mode. (R/W)                                    |
| 5   | UART_DLO_EN                        | Configures whether or not to add a turnaround delay of 1 bit before the start bit.<br>0: Not add<br>1: Add (R/W) |
| 4   | UART_DL1_EN                        | Configures whether or not to add a turnaround delay of 1 bit after the stop bit.<br>0: Not add<br>1: Add (R/W) |
| 3   | UART_RS485TX_RX_EN                 | Set this bit to enable the receiver could receive data when the transmitter is transmitting data in RS485 mode. (R/W) |
| 2   | UART_RS485RXBY_TX_EN               | 1: enable RS485 transmitter to send data when RS485 receiver line is busy. (R/W) |
| 1   | UART_DLO_EN                        |                                                                             |
| 0   | UART_DL1_EN                        |                                                                             |

```
```plaintext
GoBack

Espressif Systems          584          ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```