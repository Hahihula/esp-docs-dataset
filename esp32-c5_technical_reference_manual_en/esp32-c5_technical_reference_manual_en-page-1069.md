

```markdown
## 32.8.2 LP UART Registers

The addresses in this section are relative to LP UART base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 32.38. LP_UART_FIFO_REG (0x0000)

```text
31                                 8 7                         0
+------------------------------------------------------------------------------+
| RESERVED | LP_UART_RXFIFO_RD_BYTE |
+------------------------------------------------------------------------------+
```

LP_UART_RXFIFO_RD_BYTE Represents the data LP UART n read from FIFO.
Measurement unit: byte. (RO)

### Register 32.39. LP_UART_TOUT_CONF_SYNC_REG (0x0064)

```text
31                                 12 11                         2   1    0
+------------------------------------------------------------------------------+
| RESERVED | Oxa | LP_UART_RX_TOUT_THRD | LP_UART_RX_TOUT_FLOW_DIS | LP_UART_RX_TOUT_EN |
+------------------------------------------------------------------------------+
```

LP_UART_RX_TOUT_EN Configures whether or not to enable LP UART receiver's timeout function.
O: Disable
1: Enable
(R/W)

LP_UART_RX_TOUT_FLOW_DIS Configures whether or not to disable the idle status counter when hardware flow control is enabled.
O: Invalid. No effect
1: Disable
(R/W)

LP_UART_RX_TOUT_THRD Configures the amount of time that the bus can remain idle before timeout.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```