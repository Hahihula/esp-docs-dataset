

```markdown
## Register 32.59. LP_UART_MEM_TX_STATUS_REG (0x0068)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 17:16     |                                | (reserved)                                                                  |
| 12:11     | LP_UART_TX_SRAM_RADDR          | Represents the offset address to read TX FIFO. (RO)                          |
| 8:7       | (reserved)                     |                                                                             |
| 3:2       | LP_UART_TX_SRAM_WADDR           | Represents the offset address to write TX FIFO. (RO)                         |
| 1:0       |                                | (reserved)                                                                  |

LP_UART_TX_SRAM_WADDR  Represents the offset address to write TX FIFO. (RO)
LP_UART_TX_SRAM_RADDR   Represents the offset address to read TX FIFO. (RO)

## Register 32.60. LP_UART_MEM_RX_STATUS_REG (0x006C)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 17:16     |                                | (reserved)                                                                  |
| 12:11     | LP_UART_RX_SRAM_WADDR           | Represents the offset address to write RX FIFO. (RO)                         |
| 8:7       | (reserved)                     |                                                                             |
| 3:2       | LP_UART_RX_SRAM_RADDR           | Represents the offset address to read RX FIFO. (RO)                          |
| 1:0       |                                | (reserved)                                                                  |

LP_UART_RX_SRAM_RADDR   Represents the offset address to read RX FIFO. (RO)
LP_UART_RX_SRAM_WADDR    Represents the offset address to write RX FIFO. (RO)

## Register 32.61. LP_UART_FSM_STATUS_REG (0x0070)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31:8      | (reserved)                     |                                                                             |
| 7:4       | LP_UART_ST_UTX_OUT              | Represents the status of the transmitter. (RO)                               |
| 3:0       | LP_UART_ST_URX_OUT              | Represents the status of the receiver. (RO)                                 |

LP_UART_ST_URX_OUT  Represents the status of the receiver. (RO)
LP_UART_ST_UTX_OUT  Represents the status of the transmitter. (RO)
```