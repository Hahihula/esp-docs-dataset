

```markdown
| Register                  | Field                                                                 |
|----------------------------|------------------------------------------------------------------------|
| UART_AT_CMD_CHAR_REG      | UART_CHAR_NUM[7:0]<br>UART_AT_CMD_CHAR[7:0]                           |

## 26.5.1.3 Immediate Registers

Except those listed in Table 26.5-1 and Table 26.5-2, registers that can be configured by software are immediate registers read in APB_CLK domain, such as interrupt and FIFO configuration registers.

## 26.5.2 Detailed Steps

Figure 26.5-1 illustrates the process to program UART controllers, namely initialize UART, configure registers, enable the UART transmitter or receiver, and finish data transmission.
```

![Figure 26.5-1. UART Programming Procedures](image_path)