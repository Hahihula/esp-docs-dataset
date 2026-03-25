

# 28.7 Registers

## 28.7.1 UART Registers

The addresses in this section are relative to UART Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 28.1. UART_FIFO_REG (0x0000)

```
31                                 8 7 0
+-----------------------------------------------+
| (reserved) | UART_RXFIFO_RD_BYTE |
+-----------------------------------------------+
                 Reset
```

**UART_RXFIFO_RD_BYTE** Represents the data UART n read from FIFO.  
Measurement unit: byte. (RO)

### Register 28.2. UART_TOUT_CONF_SYNC_REG (0x0064)

```
31                                 12 11        2   1    0
+-----------------------------------------------+
| (reserved) | Oxa | UART_RX_TOUT_THRD | UART_RX_TOUT_EN |
+-----------------------------------------------+
                 Reset
```

**UART_RX_TOUT_EN** Configures whether or not to enable UART receiver's timeout function.  
0: Disable  
1: Enable  
(R/W)

**UART_RX_TOUT_THRD** Configures the amount of time that the bus can remain idle before timeout.  
Measurement unit: bit time (the time to transmit 1 bit). (R/W)