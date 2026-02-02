**Title: Chapter 19 UART Controller (UART)**

**Subtitle: Register 19.9. UART_CONFO_REG (0x20)**

**Binary Table Representation of the Register Bits**
- The table shows a binary representation for each bit in the register, with some bits labeled as "reserved".

**Register Description and Details**

- **UART_TICK_REF_ALWAYS_ON**: This register is used to select the clock; 1: APB clock; 0: REF_TICK. (R/W)
  
- **UART_DTR_INV**: Set this bit to invert the level of the UART DTR signal. (R/W)

- **UART_RTS_INV**: Set this bit to invert the level of the UART RTS signal. (R/W)

- **UART_TXD_INV**: Set this bit to invert the level of the UART Txd signal. (R/W)

- **UART_DSR_INV**: Set this bit to invert the level of the UART DSR signal. (R/W)

- **UART_CTS INV**: Set this bit to invert the level of the UART CTS signal. (R/W)

- **UART_RXD_INV**: Set this bit to invert the level of the UART Rxd signal. (R/W)

- **UART_TXFIFO_RST**: Set this bit to reset the UART transmit-FIFO. NOTICE: UART2 doesn’t have any register to reset Tx_FIFO or Rx_FIFO, and the UART1_TXFIFO_RST and UART1_RXFIFO_RST in UART1 may impact the functioning of UART2. Therefore, these two registers in UART1 should only be used when the Tx_FIFO and Rx_FIFO in UART2 do not have any data. (R/W)

- **UART_RXFIFO_RST**: Set this bit to reset the UART receive-FIFO. NOTICE: UART2 doesn’t have any register to reset Tx_FIFO or Rx_FIFO, and the UART1_TXFIFO_RST and UART1_RXFIFO_RST in UART1 may impact the functioning of UART2. Therefore, these two registers in UART1 should only be used when the Tx_FIFO and Rx_FIFO in UART2 do not have any data. (R/W)

- **UART_IRDA_EN**: Set this bit to enable the IrDA protocol. (R/W)

- **UART_TX_FLOW_EN**: Set this bit to enable the flow control function for the transmitter. (R/W)

- **UART_LOOPBACK**: Set this bit to enable the UART loopback test mode. (R/W)

- **UART_IRDA_RX_INV**: Set this bit to invert the level of the IrDA receiver. (R/W)

- **UART_IRDA_TX INV**: Set this bit to invert the level of the IrDA transmitter. (R/W)

- **UART_IRDA_WCTL**: 1: The IrDAtransmitter’s 11th bit is the same as its 10th bit; O: set IrDA transmitter’s 11th bit to 0. (R/W)

- **UART_IRDA_TX_EN**: This is the start enable bit of the IrDA transmitter. (R/W)

- **UART_IRDA_DPLX**: Set this bit to enable the IrDA loopback mode. (R/W)

- **UART_TXD_BRK**: Set this bit to enable the transmitter to send NULL, when the process of sending data is completed. (R/W)

**Footer:**
Continued on the next page...

**Document Information:** 
Espressif Systems  
Page 332  
ESP32 TRM (Version 5.6)  

**Action Links:**
- Submit Documentation Feedback