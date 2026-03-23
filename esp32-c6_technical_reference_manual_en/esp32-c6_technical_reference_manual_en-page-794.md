

```markdown
Register 27.59. LP_UART_MEM_TX_STATUS_REG (0x0068)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 17  | LP_UART_TX_SRAM_WADDR        |
| 16  |                              |
| 12  | LP_UART_TX_SRAM_RADDR        |
| 11  | (reserved)                   |
| 8   |                              |
| 7   |                              |
| 3   |                              |
| 2   |                              |
| 0   | Reset                        |

LP_UART_TX_SRAM_WADDR Represents the offset address to write TX FIFO. (RO)
LP_UART_TX_SRAM_RADDR Represents the offset address to read TX FIFO. (RO)

Register 27.60. LP_UART_MEM_RX_STATUS_REG (0x006C)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 17  |                              |
| 16  |                              |
| 12  | LP_UART_RX_SRAM_WADDR        |
| 11  | (reserved)                   |
| 8   |                              |
| 7   |                              |
| 3   |                              |
| 2   |                              |
| 0   | Reset                        |

LP_UART_RX_SRAM_RADDR Represents the offset address to read RX FIFO. (RO)
LP_UART_RX_SRAM_WADDR Represents the offset address to write RX FIFO. (RO)

Register 27.61. LP_UART_FSM_STATUS_REG (0x0070)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 8   |                              |
| 7   | LP_UART_ST_UTX_OUT           |
| 4   |                              |
| 3   | LP_UART_ST_URX_OUT           |
| 0   | Reset                        |

LP_UART_ST_URX_OUT Represents the status of the receiver. (RO)
LP_UART_ST_UTX_OUT Represents the status of the transmitter. (RO)
```