

```markdown
## 26.7 Registers

The addresses in this section are relative to UART Controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

### Register 26.1. UART_FIFO_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31:8 | reserved |
| 7:0 | UART_RXFIFO_RD_BYTE |

UART_RXFIFO_RD_BYTE UARTn accesses FIFO via this field. (RO)

### Register 26.2. UART_MEM_CONF_REG (0x0060)

| Bit | Description |
|-----|-------------|
| 31:28 | reserved |
| 27 | UART_MEM_FORCE_PU |
| 26 | UART_MEM_FORCE_PD |
| 25-16 | reserved |
| 15 | UART_RX_TOUT_THRD |
| 14-0 | reserved |

UART_RX_SIZE This field is used to configure the amount of RAM allocated for RX FIFO. The default number is 128 bytes. (R/W)

UART_TX_SIZE This field is used to configure the amount of RAM allocated for TX FIFO. The default number is 128 bytes. (R/W)

UART_RX_FLOW_THRD This field is used to configure the maximum amount of data bytes that can be received when hardware flow control works. (R/W)

UART_RX_TOUT_THRD This field is used to configure the threshold time that the receiver takes to receive one byte, in the unit of bit time (the time it takes to transfer one bit). The UART_RXFIFO_TOUT_INT interrupt will be triggered when the receiver takes more time to receive one byte with UART_RX_TOUT_EN set to 1. (R/W)

UART_MEM_FORCE_PD Set this bit to force power down UART RAM. (R/W)

UART_MEM_FORCE_PU Set this bit to force power up UART RAM. (R/W)
```