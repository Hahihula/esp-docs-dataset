**Chapter Title:**
Chapter 26 UART Controller (UART)

**Subsections and Bullet Points:**
- IrDA protocol
- High-speed data communication using DMA
- UART as wake-up source
- Software and hardware flow control

**Section Heading with Subheading:**
26.3 UART Structure

**Diagram Labels in Section "26.3 UART Structure":**
- RAM
  - UART_MEM FORCE PU
  - UART_MEM FORCE PD
  - UART_TX_SIZE
  - UART_RX_SIZE
  - UART_TXFIFO_RST
  - UART_RXFIFO_RST
- apb_wdata (pointing to UART0)
- apb_rdata (pointing to UART1)

**Figure Caption:**
Figure 26.3-1. UART Architecture Overview

**Diagram Labels in Figure "26.3-2. UART Structure":**

**RAM Section:**
- RAM
- Clock source labeled as UART_CLKDIV REG, UART_SCLK SEL REG (with a divider indicating the division of clock signal)

**UART Core Components and Connections:**
- cts_in -> Hardware Flow Control
  - rts_in
- UART_TXD INV connected to txd_out

**Transmitter Section in Diagram:**
- UART0 Rx_FIFO
  - apb_wdata (pointing towards Tx_FIFO)
  - fifo_rd data, fifo_rd
- Tx_FIFO_CTRL and Tx_FSM components with connections for flow control.

**Receiver Section in Diagram:**
- Receiver labeled as RX_FIFO
  - fifo_wr data

**Software Flow Control Components:**
- Start/Detect (1) connected to UART_RXD INV.
- Baudrate Detect, UART_LOOPBACK connection indicating wake-up and wakeup control signals. 

**Figure Caption for the second diagram in "26.3 UART Structure":**
Figure 26.3-2. UART Structure

**Footer:**
Espressif Systems
925 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback