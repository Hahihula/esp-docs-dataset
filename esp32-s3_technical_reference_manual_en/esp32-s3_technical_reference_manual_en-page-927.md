**Title:**
Chapter 26 UART Controller (UART)

**Body Text:**

- **Section Reference:** Section 26.5 explains the procedure to ensure that the configured register values are synchronized between APB_CLK domain and Core Clock domain.
  
- **Subsection Reference:** Section 26.5.2.1 explains the procedure to reset the whole UART controller. Note that it is not recommended to only reset the APB clock domain module or UART Core.

**Subtitle:**
26.4.2 UART RAM

**Diagram Description (Figure Caption):**
- **Title of Figure:** Figure 26.4-1. UART Controllers Sharing RAM
- The diagram shows a block labeled "RAM" with offsets and corresponding UART FIFO blocks:
  - offset:0 -> UART0 Tx_FIFO, 1 block, 128 bytes
  - offset:128 -> UART1 Tx_FIFO
  - offset:256 -> UART2 Tx_FIFO
  - offset:384 -> Reserved
  - offset:512 -> UART0 Rx_FIFO
  - offset:640 -> UART1 Rx_FIFO
  - offset:768 -> UART2 Rx_FIFO

**Body Text Continued:**

All three UART controllers on ESP32-S3 share 1024 x 8 bits of RAM. As Figure 26.4-1 illustrates, the RAM is divided into 8 blocks, each having 128 x 8 bits.

Figure 26.4-1 shows how many RAM blocks are allocated by default to TX and RX FIFOs for each of the three UART controllers.
- **UARTo Tx_FIFO** can be expanded up to (the whole RAM);
- **UART1 Tx_FIFO** can be increased up to 7 blocks (from offset 128 to the end address);
- **UART2 Tx_FIFO** can be increased up to 6 blocks (from offset 256 to the end address);

- **UARTo Rx_FIFO** can be expanded by increasing it from offset 0 to 255.
- **UART1 Rx_FIFO** can be increased in size, but UART1’s transmitting function cannot be used as a result.

Please note that starting addresses of all FIFOs are fixed. For example, setting UARTX_TX_SIZE of UARTO to 2 increases the size of UARTO Tx_FIFO by 128 bytes (from offset 0 to 255). In this case, UARTO Tx_FIFO takes up the default space for UART1 Tx_FIFO.

**Footer:**
Espressif Systems
927 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback