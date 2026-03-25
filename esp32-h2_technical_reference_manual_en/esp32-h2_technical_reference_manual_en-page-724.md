
```markdown
Register 28.4. UART_INT_ST_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |
|     | UART_WAKEUP_INT_ST | UART_AT_CMD_CHAR_DET_INT_ST | UART_RS485_CLASH_INT_ST | UART_RS485_FRM_ERR_INT_ST | UART_RS485_PARITY_ERR_INT_ST | UART_TX_BRK_IDLE_DONE_INT_ST | UART_SW_XOFF_INT_ST | UART_SW_XON_INT_ST | UART_RXFIFO_TOUT_INT_ST | UART_BRK_DET_INT_ST | UART_CTS_CHG_INT_ST | UART_DSR_CHG_INT_ST | UART_RXFIFO_OVF_INT_ST | UART_RXFIFO_ERR_INT_ST | UART_FRM_ERR_INT_ST | UART_PARITY_ERR_INT_ST | UART_TXFIFO_EMPTY_INT_ST | UART_RXFIFO_FULL_INT_ST | (reserved) |

UART_RXFIFO_FULL_INT_ST  The masked interrupt status of UART_RXFIFO_FULL_INT.(RO)
UART_TXFIFO_EMPTY_INT_ST  The masked interrupt status of UART_TXFIFO_EMPTY_INT. (RO)
UART_PARITY_ERR_INT_ST    The masked interrupt status of UART_PARITY_ERR_INT. (RO)
UART_FRM_ERR_INT_ST       The masked interrupt status of UART_FRM_ERR_INT. (RO)
UART_RXFIFO_OVF_INT_ST    The masked interrupt status of UART_RXFIFO_OVF_INT. (RO)
UART_DSR_CHG_INT_ST       The masked interrupt status of UART_DSR_CHG_INT. (RO)
UART_CTS_CHG_INT_ST       The masked interrupt status of UART_CTS_CHG_INT. (RO)
UART_BRK_DET_INT_ST       The masked interrupt status of UART_BRK_DET_INT. (RO)
UART_RXFIFO_TOUT_INT_ST   The masked interrupt status of UART_RXFIFO_TOUT_INT. (RO)
UART_SW_XON_INT_ST        The masked interrupt status of UART_SW_XON_INT. (RO)
UART_SW_XOFF_INT_ST       The masked interrupt status of UART_SW_XOFF_INT. (RO)
UART_GLITCH_DET_INT_ST    The masked interrupt status of UART_GLITCH_DET_INT. (RO)
UART_TX_BRK_DONE_INT_ST   The masked interrupt status of UART_TX_BRK_DONE_INT. (RO)
UART_TX_BRK_IDLE_DONE_INT_ST  The masked interrupt status of UART_TX_BRK_IDLE_DONE_INT. (RO)
UART_TX_DONE_INT_ST       The masked interrupt status of UART_TX_DONE_INT. (RO)
UART_RS485_PARITY_ERR_INT_ST  The masked interrupt status of UART_RS485_PARITY_ERR_INT. (RO)
UART_RS485_FRM_ERR_INT_ST     The masked interrupt status of UART_RS485_FRM_ERR_INT. (RO)
UART_RS485_CLASH_INT_ST       The masked interrupt status of UART_RS485_CLASH_INT. (RO)
UART_AT_CMD_CHAR_DET_INT_ST   The masked interrupt status of UART_AT_CMD_CHAR_DET_INT. (RO)
UART_WAKEUP_INT_ST            The masked interrupt status of UART_WAKEUP_INT. (RO)
```