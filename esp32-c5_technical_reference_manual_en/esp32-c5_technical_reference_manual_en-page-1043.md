

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| UART_AT_CMD_CHAR_SYNC_REG                 | AT escape sequence detection configuration                                  | 0x005C    | R/W    |

**Autobaud Register**

| Name                                      | Description                                                                 | Address   | Access |
|-------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| UART_POSPULSE_REG                         | Autobaud high pulse register                                                | 0x0074    | RO     |
| UART_NEGPULSE_REG                         | Autobaud low pulse register                                                 | 0x0078    | RO     |
| UART_LOWPULSE_REG                         | Autobaud minimum low pulse duration register                                | 0x007C    | RO     |
| UART_HIGHPULSE_REG                        | Autobaud minimum high pulse duration register                               | 0x0080    | RO     |

| Name                                      | Description                                                                 | Address   | Access |
|-------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| UART_RXD_CNT_REG                          | Autobaud edge change count register                                        | 0x0084    | RO     |

**Version Register**

| Name                                      | Description                                                                 | Address   | Access |
|-------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| UART_DATE_REG                             | UART version control register                                               | 0x008C    | R/W    |

### 32.7.2 LP UART Register Summary

The addresses in this section are relative to LP UART base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **FIFO Configuration Register**           |                                                                             |           |        |
| LP_UART_FIFO_REG                          | FIFO data register                                                          | 0x0000    | RO     |
| LP_UART_TOUT_CONF_SYNC_REG                | LP UART threshold and allocation configuration                              | 0x0064    | R/W    |
| **LP UART Interrupt Register**            |                                                                             |           |        |
| LP_UART_INT_RAW_REG                       | Raw interrupt status                                                        | 0x0004    | R/WTC/SS|
| LP_UART_INT_ST_REG                         | Masked interrupt status                                                     | 0x0008    | RO     |
| LP_UART_INT_ENA_REG                        | Interrupt enable bits                                                       | 0x000C    | R/W    |
| LP_UART_INT_CLR_REG                        | Interrupt clear bits                                                        | 0x0010    | WT     |
| **Configuration Register**                |                                                                             |           |        |
| LP_UART_CLKDIV_SYNC_REG                   | Clock divider configuration                                                 | 0x0014    | R/W    |
| LP_UART_RX_FILT_REG                        | RX filter configuration                                                     | 0x0018    | R/W    |
| LP_UART_CONFO_SYNC_REG                     | Configuration register 0                                                    | 0x0020    | R/W    |
| LP_UART_CONF1_REG                          | Configuration register 1                                                   | 0x0024    | R/W    |
| LP_UART_HWFC_CONF_SYNC_REG                 | Hardware flow control configuration                                        | 0x002C    | R/W    |
| LP_UART_SLEEP_CONFO_REG                    | LP UART sleep configuration register 0                                     | 0x0030    | R/W    |
| LP_UART_SLEEP_CONF1_REG                    | LP UART sleep configuration register 1                                     | 0x0034    | R/W    |
| LP_UART_SLEEP_CONF2_REG                    | LP UART sleep configuration register 2                                     | 0x0038    | R/W    |
| LP_UART_SWFC_CONFO_SYNC_REG                | Software flow control character configuration                               | 0x003C    | varies |
| LP_UART_SWFC_CONF1_REG                     | Software flow control character configuration                               | 0x0040    | R/W    |
| LP_UART_TXBRK_CONF_SYNC_REG                | TX break character configuration                                           | 0x0044    | R/W    |
| LP_UART_IDLE_CONF_SYNC_REG                 | Frame end idle time configuration                                          | 0x0048    | R/W    |
| LP_UART_DELAY_CONF_SYNC_REG                | RS485 mode configuration                                                   | 0x004C    | R/W    |
```