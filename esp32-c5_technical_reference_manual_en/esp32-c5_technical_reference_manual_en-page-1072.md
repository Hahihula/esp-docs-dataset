
```markdown
Register 32.41. LP_UART_INT_ST_REG (0x0008)

| Bit Field | Description |
|-----------|-------------|
| 31        | (reserved) |
| 30        | LP_UART_WAKEUP_INT_ST |
| 29        | LP_UART_AT_CMD_CHAR_DET_INT_ST |
| 28        | (reserved) |
| 27        | LP_UART_TX_DONE_INT_ST |
| 26        | LP_UART_TX_BRK_DONE_INT_ST |
| 25        | LP_UART_TX_SW_XON_INT_ST |
| 24        | LP_UART_TX_SW_OFF_INT_ST |
| 23        | LP_UART_GLITCH_DET_INT_ST |
| 22        | LP_UART_RXFIFO_TOUT_INT_ST |
| 21        | LP_UART_BRK_DET_INT_ST |
| 20        | LP_UART_CTS_CHG_INT_ST |
| 19        | LP_UART_DSR_CHG_INT_ST |
| 18        | LP_UART_RXFIFO_OVF_INT_ST |
| 17        | LP_UART_FRM_ERR_INT_ST |
| 16        | LP_UART_PARITY_ERR_INT_ST |
| 15        | LP_UART_TXFIFO_EMPTY_INT_ST (RO) |
| 14        | LP_UART_RXFIFO_FULL_INT_ST (RO) |
| 13-7      | (reserved) |
| 6         | LP_UART_TX_BRK_IDLE_DONE_INT_ST (masked interrupt status of LP_UART_TX_BRK_IDLE_DONE_INT. (RO)) |
| 5         | LP_UART_TX_DONE_INT_ST (masked interrupt status of LP_UART_TX_DONE_INT. (RO)) |
| 4         | LP_UART_AT_CMD_CHAR_DET_INT_ST (masked interrupt status of LP_UART_AT_CMD_CHAR_DET_INT. (RO)) |
| 3         | LP_UART_WAKEUP_INT_ST (masked interrupt status of LP_UART_WAKEUP_INT. (RO)) |
| 2-0       | Reserved |

LP_UART_RXFIFO_FULL_INT_ST The masked interrupt status of LP_UART_RXFIFO_FULL_INT.(RO)
LP_UART_TXFIFO_EMPTY_INT_ST The masked interrupt status of LP_UART_TXFIFO_EMPTY_INT.
(RO)
LP_UART_PARITY_ERR_INT_ST The masked interrupt status of LP_UART_PARITY_ERR_INT. (RO)
LP_UART_FRM_ERR_INT_ST The masked interrupt status of LP_UART_FRM_ERR_INT. (RO)
LP_UART_RXFIFO_OVF_INT_ST The masked interrupt status of LP_UART_RXFIFO_OVF_INT. (RO)
LP_UART_DSR_CHG_INT_ST The masked interrupt status of LP_UART_DSR_CHG_INT. (RO)
LP_UART_CTS_CHG_INT_ST The masked interrupt status of LP_UART_CTS_CHG_INT. (RO)
LP_UART_BRK_DET_INT_ST The masked interrupt status of LP_UART_BRK_DET_INT. (RO)
LP_UART_RXFIFO_TOUT_INT_ST The masked interrupt status of LP_UART_RXFIFO_TOUT_INT. (RO)
LP_UART_SW_XON_INT_ST The masked interrupt status of LP_UART_SW_XON_INT. (RO)
LP_UART_SW_OFF_INT_ST The masked interrupt status of LP_UART_SW_OFF_INT. (RO)
LP_UART_GLITCH_DET_INT_ST The masked interrupt status of LP_UART_GLITCH_DET_INT. (RO)
LP_UART_TX_BRK_DONE_INT_ST The masked interrupt status of LP_UART_TX_BRK_DONE_INT.
(RO)

LP_UART_TX_BRK_IDLE_DONE_INT_ST The masked interrupt status of LP_UART_TX_BRK_IDLE_DONE_INT. (RO)
LP_UART_TX_DONE_INT_ST The masked interrupt status of LP_UART_TX_DONE_INT. (RO)

LP_UART_AT_CMD_CHAR_DET_INT_ST The masked interrupt status of LP_UART_AT_CMD_CHAR_DET_INT. (RO)

LP_UART_WAKEUP_INT_ST The masked interrupt status of LP_UART_WAKEUP_INT. (RO)
```