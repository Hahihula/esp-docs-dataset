

```markdown
| Register                     | Field                                                                 |
|------------------------------|------------------------------------------------------------------------|
| UART_FLOW_CONF_REG          | UART_SEND_XOFF                                                        |
|                              | UART_SEND_XON                                                         |
|                              | UART_FORCE_XOFF                                                       |
|                              | UART_FORCE_XON                                                        |
|                              | UART_XONOFF_DEL                                                       |
|                              | UART_SW_FLOW_CON_EN                                                   |
| UART_TXBRK_CONF_REG         | UART_RS485_TX_DLY_NUM[3:0]                                             |
|                              | UART_RS485_RX_DLY_NUM                                                 |
|                              | UART_RS485RXBY_TX_EN                                                  |
|                              | UART_RS485TX_RX_EN                                                    |
|                              | UART_DLI_EN                                                           |
|                              | UART_DLO_EN                                                           |
|                              | UART_RS485_EN                                                         |

Table 26.5-1 – cont’d from previous page
```

## 26.5.1.2 Static Registers

Static registers, though also read in Core Clock domain, would not change dynamically when UART controllers are at work, so they do not implement the clock domain crossing design. These registers must be configured when the UART transmitter or receiver is not at work. In this case, software can turn off the clock for the UART transmitter or receiver, so that static registers are not sampled in their metastable state. When software turns on the clock, the configured values are stable to be correctly sampled. Static registers as listed in Table 26.5-2 are configured as follows:

*   Turn off the clock for the UART transmitter by clearing `UART_TX_SCLK_EN`, or the clock for the UART receiver by clearing `UART_RX_SCLK_EN`, depending on which one (transmitter or receiver) is not at work;
*   Configure static registers;
*   Turn on the clock for the UART transmitter by writing 1 to `UART_TX_SCLK_EN`, or the clock for the UART receiver by writing 1 to `UART_RX_SCLK_EN`.

Table 26.5-2. UARTn Static Registers

| Register                     | Field                                                                 |
|------------------------------|------------------------------------------------------------------------|
| UART_RX_FILT_REG             | UART_GLITCH_FILT_EN                                                   |
|                              | UART_GLITCH_FILT[7:0]                                                 |
| UART_SLEEP_CONF_REG          | UART_ACTIVE_THRESHOLD[9:0]                                            |
| UART_SWFC_CONF_INFO_REG      | UART_XOFF_CHAR[7:0]                                                   |
| UART_SWFC_CONF1_REG          | UART_XON_CHAR[7:0]                                                    |
| UART_IDLE_CONF_REG           | UART_TX_IDLE_NUM[9:0]                                                 |
| UART_AT_CMD_PRECNT_REG       | UART Prä_IDLE_NUM[15:0]                                               |
| UART_AT_CMD_POSTCNT_REG      | UART_POST_IDLE_NUM[15:0]                                              |
| UART_AT_CMD_GAPTOUT_REG      | UART_RX_GAP_TOUT[15:0]                                                |

cont’d on next page
```