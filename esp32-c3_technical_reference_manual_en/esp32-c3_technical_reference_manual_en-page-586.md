

```markdown
Register 26.20. UART_MEM_TX_STATUS_REG (0x0064)

| 31 | 21 | 20 | 11 | 10 | 9 | 0 |
|----:|----:|----:|----:|----:|---:|---:|
|    |    |    | UART_TX_RADDR | (reserved) | UART_APB_TX_WADDR |

UART_APB_TX_WADDR This field stores the offset address in TX FIFO when software writes TX FIFO via APB. (RO)

UART_TX_RADDR This field stores the offset address in TX FIFO when TX FSM reads data via Tx_FIFO_Ctrl. (RO)


Register 26.21. UART_MEM_RX_STATUS_REG (0x0068)

| 31 | 21 | 20 | 11 | 10 | 9 | 0 |
|----:|----:|----:|----:|----:|---:|---:|
|    |    |    | UART_RX_WADDR | (reserved) | UART_APB_RX_RADDR |

UART_APB_RX_RADDR This field stores the offset address in RX FIFO when software reads data from RX FIFO via APB. UART0 is 0x200. UART1 is 0x280. (RO)

UART_RX_WADDR This field stores the offset address in RX FIFO when Rx_FIFO_Ctrl writes RX FIFO. (RO)


Register 26.22. UART FSM_STATUS_REG (0x006C)

| 31 | 30 | 29 | ... | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|-----:|---:|---:|---:|---:|---:|
|    | UART_ST_UTX_OUT | (reserved) | UART_ST_URX_OUT |

UART_ST_URX_OUT This is the status field of the receiver. (RO)

UART_ST_UTX_OUT This is the status field of the transmitter. (RO)
```