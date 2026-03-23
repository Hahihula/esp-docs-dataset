

```markdown
| Name | Description | Address | Access |
|:-------------------------|:--------------------------------------------------------------------------|:---------|:--------|
| FIFO Configuration | | | |
| UART_FIFO_REG | FIFO data register | 0x0000 | RO |
| UART_MEM_CONF_REG | UART threshold and allocation configuration | 0x0060 | R/W |
| UART Interrupt Register | | | |
| UART_INT_RAW_REG | Raw interrupt status | 0x0004 | R/WTC/SS |
| UART_INT_ST_REG | Masked interrupt status | 0x0008 | RO |
| UART_INT_ENA_REG | Interrupt enable bits | 0x000C | R/W |
| UART_INT_CLR_REG | Interrupt clear bits | 0x0010 | WT |
| Configuration Register | | | |
| UART_CLKDIV_REG | Clock divider configuration | 0x0014 | R/W |
| UART_RX_FILTER_REG | RX filter configuration | 0x0018 | R/W |
| UART_CONF0_REG | Configuration register 0 | 0x0020 | R/W |
| UART_CONF1_REG | Configuration register 1 | 0x0024 | R/W |
| UART_FLOW_CONF_REG | Software flow control configuration | 0x0034 | varies |
| UART_SLEEP_CONF_REG | Sleep mode configuration | 0x0038 | R/W |
| UART_SWFC_CONF0_REG | Software flow control character configuration | 0x003C | R/W |
| UART_SWFC_CONF1_REG | Software flow control character configuration | 0x0040 | R/W |
| UART_TXBRK_CONF_REG | TX break character configuration | 0x0044 | R/W |
| UART_IDLE_CONF_REG | Frame end idle time configuration | 0x0048 | R/W |
| UART_RS485_CONF_REG | RS485 mode configuration | 0x004C | R/W |
| UART_CLK_CONF_REG | UART core clock configuration | 0x0078 | R/W |
| Status Register | | | |
| UART_STATUS_REG | UART status register | 0x001C | RO |
| UART_MEM_TX_STATUS_REG | TX FIFO write and read offset address | 0x0064 | RO |
| UART_MEM_RX_STATUS_REG | RX FIFO write and read offset address | 0x0068 | RO |
| UART_FSM_STATUS_REG | UART transmitter and receiver status | 0x006C | RO |
| Autobaud Register | | | |
| UART_LOWPULSE_REG | Autobaud minimum low pulse duration register | 0x0028 | RO |
| UART_HIGHPULSE_REG | Autobaud minimum high pulse duration register | 0x002C | RO |
| UART_RXD_CNT_REG | Autobaud edge change count register | 0x0030 | RO |
| UART_POSPULSE_REG | Autobaud high pulse register | 0x0070 | RO |
| UART_NEGPULSE_REG | Autobaud low pulse register | 0x0074 | RO |
| AT Escape Sequence Selection Configuration | | | |
| UART_AT_CMD_PRECNT_REG | Pre-sequence timing configuration | 0x0050 | R/W |
| UART_AT_CMD_POSTCNT_REG | Post-sequence timing configuration | 0x0054 | R/W |
```