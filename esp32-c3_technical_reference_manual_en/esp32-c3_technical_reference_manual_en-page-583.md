

```markdown
Register 26.13. UART_SWFC_CONF0_REG (0x003C)

| Bit Range | Description                |
|-----------|----------------------------|
| 17-16     | UART_XOFF_CHAR             |
| 9-8       | UART_XOFF_THRESHOLD        |
| 0-0       | Reset                      |

UART_XOFF_THRESHOLD When the number of data bytes in RX FIFO is more than the value of this field with UART_SW_FLOW_CON_EN set to 1, the transmitter sends an XOFF character. (R/W)

UART_XOFF_CHAR This field stores the XOFF flow control character. (R/W)


Register 26.14. UART_SWFC_CONF1_REG (0x0040)

| Bit Range | Description                |
|-----------|----------------------------|
| 17-16     | UART_XON_CHAR              |
| 9-8       | UART_XON_THRESHOLD         |
| 0-0       | Reset                      |

UART_XON_THRESHOLD When the number of data bytes in RX FIFO is less than the value of this field with UART_SW_FLOW_CON_EN set to 1, the transmitter sends an XON character. (R/W)

UART_XON_CHAR This field stores the XON flow control character. (R/W)


Register 26.15. UART_TXBRK_CONF_REG (0x0044)

| Bit Range | Description                |
|-----------|----------------------------|
| 7-0       | UART_TX_BRK_NUM            |
| 31        | Reset                      |

UART_TX_BRK_NUM This field is used to configure the number of 0 to be sent after the process of sending data is done. It is active when UART_TXD_BRK is set to 1. (R/W)
```