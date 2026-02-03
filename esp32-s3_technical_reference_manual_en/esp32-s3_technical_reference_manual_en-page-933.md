Title: Chapter 26 UART Controller (UART)

Link: GoBack

Figure Caption:
- Figure 26.4-7, The Timing Diagram of Encoding and Decoding in SIR mode.

Body Text:

The IrDA transceiver is half-duplex, meaning that it cannot send and receive data simultaneously. As shown in
Figure 26.4-8, IrDA function is enabled by setting UART_IRDA_EN. When UART_IRDA_TX_EN is set (high), the
IrDA transceiver is enabled to send data and not allowed to receive data; when UART_IRDA_TX_EN is reset
(low), the IrDA transceiver is enabled to receive data and not allowed to send data.

Figure Caption:
- Figure 26.4-8, IrDA Encoding and Decoding Diagram

Subtitles:

26.4.8 Wake-up

Body Text:

UART0 and UART1 can be set as a wake-up source for Light-sleep mode. To be specific Wakeup_Ctrl counts
up the rising edges of rxd_in, and when this count is equal to or greater than UART_ACTIVE_THRESHOLD + 3,
a wake_up signal is generated and sent to RTC, which then wakes ESP32-S3 up.

After the chip is woken up by UART, it is necessary to clear the wake_up signal by transmitting data to UART in
Active mode or resetting the whole UART, otherwise the number of rising edges required for the next wakeup
will be reduced.

26.4.9 Loopback Test

Body Text:

UARTn supports loopback testing, which can be enabled by setting UART_LOOPBACK. When loopback testing
is enabled, UART output signal rxd_out is connected to its input signal rxd_in, rtsn_out is connected to

Footer:
- Espresso Systems
- 933 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)

The image contains two diagrams labeled as Figure 26.4-7 and Figure 26.4-8.

Figure 26.4-7 shows a timing diagram with labels for UART Tx, IrDA Tx, Bit Time, IR Frame, UART Rx, Stop Bit, Start/Stop bits in the context of UART frame structure.
Figure 26.4-8 illustrates an encoding and decoding process involving UART, IrDA components (IrDA Enc, IrDA Dec), and connections between them.

The text describes how to configure UART for wake-up functionality based on rising edge counts from specific signals rxd_in or txd_in in the context of light-sleep mode.
It also explains loopback testing configuration where UART output signal is connected back into its input.