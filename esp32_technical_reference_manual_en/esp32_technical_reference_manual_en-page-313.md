**Chapter Title:**
Chapter 19 UART Controller (UART)

**Body Text:**

configuring the UART_RXD INV register. Baudrate_Detect measures the baud rate of the input signal by measuring the minimum pulse width of the input bit stream. Start_Detect is used to detect a START bit in a frame of incoming data. After detecting the START bit, RX_FSM stores data retrieved from the received frame into Rx_FIFO through Rx_FIFO_Ctrl.

Software can read data in the Rx_FIFO through the APB. In order to free the CPU from engaging in data transfer operations, the DMA can be configured for sending or receiving data.
HW_Flow_Ctrl is able to control the data flow of rxd_in and txd_out through standard UART RTS and CTS flow control signals (rtsn_out and ctsn_in). SW_Flow_Ctrl controls the data flow by inserting special characters in the incoming and outgoing data flow. When UART is in Light-sleep mode (refer to Chapter Low-Power Management), Wakeup_Ctrl will start counting pulses in rxd_in. When the number or positive edges of Rx_D signal is greater than or equal to (UART_ACTIVE_THRESHOLD+2), a wake-up signal will be generated and sent to RTC. RTC will then wake up the UART controller. Note that only UART1 and UART2 support Light-sleep mode and that rxd_in cannot be input through GPIO Matrix but only through IO_MUX.

**Subsection Title:**
19.3.3 UART RAM

**Diagram Description (Figure 19.3-2):**
UART Shared RAM
```
RAM
offset 0 -> block
UART0 Tx_FIFO
offset 128
UART1 Tx_FIFO
offset 256
UART2 Tx_FIFO
offset 384
UART0 Rx_FIFO
offset 512
UART1 Rx_FIFO
offset 640
UART2 Rx_FIFO
offset 768

Figure 19.3-2. UART Shared RAM
```

**Body Text:**

Three UART controllers share a 1024 x 8-bit RAM space. As illustrated in Figure 19.3-2, RAM is allocated in different blocks. One block holds 128 x 8-bit data. Figure 19.3-2 illustrates the default RAM allocated to Tx_FIFO and Rx_FIFO of the three UART controllers. Tx_FIFO of UARTn can be extended by setting UARTn_TX_SIZE, while Rx_FIFO of UARTn can be extended by setting UARTn_RX_SIZE.

**Notice:**
Extending the FIFO space of a UART controller may take up the FIFO space of another UART controller.
If none of the UART controllers is active, setting UART_MEM_PD, UART1_MEM_PD, and UART2_MEM_PD can prompt the RAM to enter low-power mode. In UART0, bit UART_TXFIFO_RST and bit UART_RXFIFO_RST can be set to reset Tx_FIFO or Rx_FIFO respectively. In UART1, bit UART1_TXFIFO_RST and bit UART1_RXFIFO_RST can be set to reset Tx_FIF0 or Rx_FIFO respectively.

**Footer:**
Espressif Systems
313 ESP32 TRM (Version 5.6)
Submit Documentation Feedback