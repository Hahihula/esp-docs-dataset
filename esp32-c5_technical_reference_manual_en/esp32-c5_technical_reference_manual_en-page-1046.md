

```markdown
Chapter 32 UART Controller (UART)

GoBack

## 32.8 Registers

### 32.8.1 UART Registers

The addresses in this section are relative to UART Controller base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 32.1. UART_FIFO_REG (0x0000)

| Bit 31 | ... | 8 | 7 | ... | 0 |
|--------|-----|---|---|-----|---|
| (reserved) | ... | UART_RXFIFO_RD_BYTE | Reset |

UART_RXFIFO_RD_BYTE Represents the data UARTn reads from FIFO.
Measurement unit: byte. (RO)

Register 32.2. UART_TOUT_CONF_SYNC_REG (0x0064)

| Bit 31 | ... | 12 | 11 | 2 | 1 | 0 |
|--------|-----|----|----|---|---|---|
| (reserved) | ... | Oxa | 0 | UART_RX_TOUT_THRD | UART_RX_TOUT_FLOW_DIS | UART_RX_TOUT_EN | Reset |

UART_RX_TOUT_EN Configures whether or not to enable UART receiver’s timeout function.
O: Disable
1: Enable
(R/W)

UART_RX_TOUT_FLOW_DIS Configures whether or not to disable the idle status counter when hardware flow control is enabled.
O: Enable
1: Disable
(R/W)

UART_RX_TOUT_THRD Configures the amount of time that the bus can remain idle before timeout.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```