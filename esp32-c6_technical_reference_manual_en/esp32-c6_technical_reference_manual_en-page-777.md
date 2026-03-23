

```markdown
Register 27.36. UART_REG_UPDATE_REG (0x0098)

UART_REG_UPDATE Configures whether or not to synchronize registers.
O: Not synchronize
1: Synchronize
(R/W/SC)

Register 27.37. UART_ID_REG (0x009C)

UART_ID Configures the UART ID. (R/W)
```

## 27.7.2 LP UART Registers

The addresses in this section are relative to LP UART base address provided in Table 5.3-2 in Chapter 5 System and Memory.

Register 27.38. LP_UART_FIFO_REG (0x0000)

LP_UART_RXFIFO_RD_BYTE Represents the data LP UART n read from FIFO.
Measurement unit: byte. (RO)
```