

```markdown
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| FIFO Configuration Register | | | |
| UART_FIFO_REG | FIFO data register | 0x0000 | RO |
| UART_TOUT_CONF_SYNC_REG | UART threshold and allocation configuration | 0x0064 | R/W |
| UART Interrupt Register | | | |
| UART_INT_RAW_REG | Raw interrupt status | 0x0004 | R/WTC/SS |
| UART_INT_ST_REG | Masked interrupt status | 0x0008 | RO |
| UART_INT_ENA_REG | Interrupt enable bits | 0x000C | R/W |
| UART_INT_CLR_REG | Interrupt clear bits | 0x0010 | WT |
| Configuration Register | | | |
| UART_CLKDIV_SYNC_REG | Clock divider configuration | 0x0014 | R/W |
| UART_RX_FILT_REG | RX filter configuration | 0x0018 | R/W |
| UART_CONFO_SYNC_REG | Configuration register 0 | 0x0020 | R/W |
| UART_CONF1_REG | Configuration register 1 | 0x0024 | R/W |
| UART_HWFC_CONF_SYNC_REG | Hardware flow control configuration | 0x002C | R/W |
| UART_SLEEP_CONFO_REG | UART sleep configuration register 0 | 0x0030 | R/W |
| UART_SLEEP_CONF1_REG | UART sleep configuration register 1 | 0x0034 | R/W |
| UART_SLEEP_CONF2_REG | UART sleep configuration register 2 | 0x0038 | R/W |
| UART_SWFCO_CONF_SYNC_REG | Software flow control character configuration | 0x003C | varies |
| UART_SWFC_CONF1_REG | Software flow control character configuration | 0x0040 | R/W |
| UART_TXBRK_CONF_SYNC_REG | TX break character configuration | 0x0044 | R/W |
| UART_IDLE_CONF_SYNC_REG | Frame end idle time configuration | 0x0048 | R/W |
| UART_RS485_CONF_SYNC_REG | RS485 mode configuration | 0x004C | R/W |
| UART_CLK_CONF_REG | UART core clock configuration | 0x0088 | R/W |
| UART_REG_UPDATE_REG | UART register configuration update | 0x0098 | R/W/SC |
| UART_ID_REG | UART ID register | 0x009C | R/W |
| Status Register | | | |
| UART_STATUS_REG | UART status register | 0x001C | RO |
| UART_MEM_TX_STATUS_REG | TX FIFO write and read offset address | 0x0068 | RO |
| UART_MEM_RX_STATUS_REG | Rx FIFO write and read offset address | 0x006C | RO |
| UART_FSM_STATUS_REG | UART transmit and receive status | 0x0070 | RO |
| UART_AFIFO_STATUS_REG | UART asynchronous FIFO status | 0x0090 | RO |
| AT Escape Sequence Selection Configuration Register | | | |
| UART_AT_CMD_PRECNT_SYNC_REG | Pre-sequence timing configuration | 0x0050 | R/W |
| UART_AT_CMD_POSTCNT_SYNC_REG | Post-sequence timing configuration | 0x0054 | R/W |
| UART_AT_CMD_GAPTOUT_SYNC_REG | Timeout configuration | 0x0058 | R/W |
```