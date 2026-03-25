

# 25.8 Registers

## 25.8.1 UART Registers

The addresses in this section are relative to UART Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 25.1. UART_FIFO_REG (0x0000)

UART_RXFIFO_RD_BYTE Represents the data UARTn reads from FIFO.
Measurement unit: byte. (RO)

Register 25.2. UART_TOUT_CONF_SYNC_REG (0x0064)

UART_RX_TOUT_EN Configures whether or not to enable UART receiver's timeout function.
O: Disable
1: Enable
(R/W)

UART_RX_TOUT_FLOW_DIS Configures whether or not to disable the idle status counter when hardware flow control is enabled.
O: Enable
1: Disable
(R/W)

UART_RX_TOUT_THRD Conf igures the amount of time that the bus can remain idle before timeout.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)