

```markdown
Figure 28.4-6. The Timing Diagram of Encoding and Decoding in SIR mode


The IrDA transceiver is half-duplex, meaning that it cannot send and receive data simultaneously. As shown in Figure 28.4-7, IrDA function is enabled by setting UART_IRDA_EN. When UART_IRDA_TX_EN is set to 1, the IrDA transceiver is enabled to send data and not allowed to receive data; when UART_IRDA_TX_EN is reset to 0, the IrDA transceiver is enabled to receive data and not allowed to send data.


Figure 28.4-7. IrDA Encoding and Decoding Diagram


28.4.8 Wake-up

UART can be set as wake-up source. When a UART controller is in Light-sleep mode, a wake_up signal can be generated in four ways and be sent to the RTC module, which then wakes up ESP32-H2.

*   `UART_WK_MODE_SEL = 0`: When all the clocks are disabled, the chip can be woken up by reverting RXD for multiple cycles until the number of positive edges is greater than or equal to `UART_ACTIVE_THRESHOLD + 3`.
*   `UART_WK_MODE_SEL = 1`: UART Core keeps working, so the UART receiver can still receive data and store the received data in RX FIFO. When the number of data bytes in RX FIFO is greater than `UART_RX_WAKE_UP_THRD`, the chip can be woken up from the Light-sleep mode.
*   `UART_WK_MODE_SEL = 2`: When the UART receiver detects a start bit, the chip will be woken up.
```