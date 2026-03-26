

```markdown
Register 42.59. LP_UART_MEM_RX_STATUS_REG (0x006C)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 17  | LP_UART_RX_SRAM_WADDR        |
| 16  | (reserved)                   |
| 12  | LP_UART_RX_SRAM_RADDR        |
| 8   | (reserved)                   |
| 7   | (reserved)                   |
| 3   | (reserved)                   |
| 2   | (reserved)                   |
| 0   | Reset                        |

LP_UART_RX_SRAM_RADDR Represents the offset address to read RX FIFO. (RO)
LP_UART_RX_SRAM_WADDR Represents the offset address to write RX FIFO. (RO)

Register 42.60. LP_UART FSM_STATUS_REG (0x0070)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 8   | (reserved)                   |
| 7   | LP_UART_ST_UTX_OUT           |
| 4   | LP_UART_ST_URX_OUT           |
| 3   | (reserved)                   |
| 0   | Reset                        |

LP_UART_ST_URX_OUT Represents the status of the receiver. (RO)
LP_UART_ST_UTX_OUT Represents the status of the transmitter. (RO)
```