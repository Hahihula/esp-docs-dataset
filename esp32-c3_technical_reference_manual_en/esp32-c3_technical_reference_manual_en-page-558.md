

```markdown
Figure 26.4-7. The Timing Diagram of Encoding and Decoding in SIR mode


The IrDA transceiver is half-duplex, meaning that it cannot send and receive data simultaneously. As shown in Figure 26.4-8, IrDA function is enabled by setting UART_IRDA_EN. When UART_IRDA_TX_EN is set (high), the IrDA transceiver is enabled to send data and not allowed to receive data; when UART_IRDA_TX_EN is reset (low), the IrDA transceiver is enabled to receive data and not allowed to send data.


Figure 26.4-8. IrDA Encoding and Decoding Diagram


## 26.4.8 Wake-up

UART0 and UART1 can be set as wake-up source. When a UART controller is in Light-sleep mode, Wakeup_Ctrl counts up the rising edges of rx'd_in. When the number of rising edges is equal to or greater than (UART_ACTIVE_THRESHOLD + 3), a wake_up signal is generated and sent to RTC, which then wakes up ESP32-C3.

After the chip is woken up by UART, it is necessary to clear the wake_up signal by transmitting data to UART in Active mode or resetting the whole UART, otherwise the number of rising edges required for the next wakeup will be reduced.
```