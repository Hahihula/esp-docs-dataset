**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
GoBack

**Subsection Titles and Descriptions with Registers Information:**

1. **Register 26.20. UART_MEM_TX_STATUS_REG (0x0064)**
   - **Field Description:** 
     - `UART_APB_TX_WADDR`: This field stores the offset address in TX FIFO when software writes TX FIFO via APB.
       - Access: Read Only
     - `UART_TX_RADDR`: This field stores the offset address in TX FIFO where TX FSM reads data via Tx_FIFO_Ctrl.

2. **Register 26.21. UART_MEM_RX_STATUS_REG (0x0068)**
   - **Field Description:** 
     - `UART_APB_RX_RADDR`: This field stores the offset address in RX FIFO when software reads data from RX FIFO via APB.
       - UART0 is set to 0x200, UART1 is set to 0x280, UART2 is set to 0x300. (Read Only)
     - `UART_RX_WADDR`: This field stores the offset address in RX FIFO when Rx_FIFO_Ctrl writes RX FIFO.
       - UART0 is set to 0x200, UART1 is set to 0x280, UART2 is set to 0x300. (Read Only)

3. **Register 26.22. UART_FSM_STATUS_REG (0x006C)**
   - **Field Description:** 
     - `UART_ST_URX_OUT`: This field indicates the status of the receiver.
       - Access: Read Only
     - `UART_ST_UTX_OUT`: This field is related to the transmitter's status.

**Footer Information:**
Espressif Systems  
962 ESP32-S3 TRM (Version 1.7)  

**Link Texts:** 
- Submit Documentation Feedback