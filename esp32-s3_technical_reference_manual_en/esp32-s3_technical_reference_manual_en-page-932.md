**Title:**
Chapter 26 UART Controller (UART)

**Diagram Title and Description:**
Figure 26.4-6. Driver Control Diagram in RS485 Mode

**Section Heading:**
26.4.6.2 Turnaround Delay

**Body Text:**
By default, all three UART controllers work in receiver mode. When a UART controller is switched from transmitter mode to receiver mode, the RS485 protocol requires a turnaround delay of one cycle after the stop bit. The UART transmitter supports adding a turnaround delay of one cycle not only before the start bit but also after the stop bit. When UART_DLO_EN is set, a turnaround delay of one cycle is added before the start bit; when UART_DL1_EN is set, a turnaround delay of one cycle is added after the stop bit.

**Section Heading:**
26.4.6.3 Bus Snooping

**Body Text:**
In a two-wire multidrop network, UART controllers support bus snooping if RE of the external RS485 transceiver is 0. By default, a UART controller is not allowed to transmit and receive data simultaneously. If UART_RS485_TX_RX_EN is set and the external RS485 transceiver is configured as in Figure 26.4-6, a UART controller may receive data in transmitter mode and snoop the bus. If UART_RS485_RXBY_TX_EN is set, a UART controller may transmit data in receiver mode.

All three UART controllers can snoop the data sent by themselves. In transmitter mode, when a UART controller monitors a collision between the data sent and the data received, a UART_RS485_CLASH_INT interrupt is generated; when it monitors a data frame error, a UART_RS485_FRM_ERR_INT interrupt is generated; when it monitors a polarity error, a UART_RS485_PARITY_ERR_INT is generated.

**Section Heading:**
26.4.7 IrDA

**Body Text:**
IrDA protocol consists of three layers, namely the physical layer, the link access protocol, and the link management protocol. The three UART controllers implement IrDA’s physical layer. In IrDA encoding, a UART controller supports data rates up to 115.2 kbit/s (SIR, or serial infrared mode). As shown in Figure 26.4-7, the IrDA encoder converts a NRZ (non-return to zero code) signal to a RZI (return to zero inverted code) signal and sends it to the external driver and infrared LED. This encoder uses modulated signals whose pulse width is 3/16 bits to indicate logic “0”, and low levels to indicate logic “1”. The IrDA decoder receives signals from the infrared receiver and converts them to NRZ signals. In most cases, the receiver is high when it is idle, and the encoder output polarity is the opposite of the decoder input polarity. If a low pulse is detected, it indicates that a start bit has been received.

When IrDA function is enabled, one bit is divided into 16 clock cycles. If the bit to be sent is zero, then the 9th, 10th and 11th clock cycle are high.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)