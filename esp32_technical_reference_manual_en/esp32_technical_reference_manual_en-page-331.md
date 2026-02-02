**Title: Chapter 19 UART Controller (UART)**

**Subtitle: Register 19.8. UART_STATUS_REG (0x1C)**

**Diagram Description:**  
A bit map diagram showing the layout of the UART_STATUS_REG register with labels for each bit.

- **UART_TXD**: This bit represents the level of the internal UART RxD signal.
- **UART_RTSN**: This bit corresponds to the level of the internal UART CTS signal (RO).
- **UART_DTRN**: This bit corresponds to the level of the internal UART DSR signal. (RO)
- **UART_ST_UTX_OUT**: This register stores the state of the transmitter's finite state machine.
  - TX_IDLE: 1; TX_STRT: 2; TX_DAT0: 3; TX_DAT1: 4; TX_DAT2: 5; TX_DAT3: 6; TX_DAT4: 7;
  - TX_DAT5: 8; TX_DAT6: 9; TX_DAT7: 10; TX_PRTY: 11; TX_STP1: 12; TX_STP2: 13; TX_DLO: 14;
  - TX_DL1. (RO)
- **UART_TXFIFO_CNT**: (tx_mem_cnt, txfifo_cnt) stores the number of bytes of valid data in transmit FIFO.
  - tx_mem_cnt stores the three most significant bits,
  - txfifo_cnt stores the eight least significant bits. (RO)
- **UART_RXD**: This bit corresponds to the level of the internal UART RxD signal. (RO)
- **UART_CTSN**: This bit corresponds to the level of the internal UART CTS signal.
- **UART_DSRN**: This bit corresponds to the level of the internal UART DSR signal.

**UART_ST_URX_OUT**: This register stores the value of the receiver's finite state machine. 
  - RX_IDLE: 1; RX_STRT: 2; RX_DAT0: 3; RX_DAT1: 4; RX_DAT2: 5; RX_DAT3: 6;
  - RX_DAT4: 7; RX_DAT5: 8; RX_DAT6: 9; RX_DAT7: 10; RX_PRTY: 11; RX_STP1: 12; RX_STP2: 13; RX_DL1. (RO)

**UART_RXFIFO_CNT**: (rx_mem_cnt, rxfif0_cnt) stores the number of bytes of valid data in the receive FIFO.
- rx_mem_cnt register stores the three most significant bits,
- rxfif0_cnt stores the eight least significant bits.

**Footer:**  
Espressif Systems  
331 ESP32 TRM (Version 5.6)

**Link:** Submit Documentation Feedback