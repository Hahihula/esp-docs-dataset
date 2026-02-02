**Title:**
Chapter 19 UART Controller (UART)

**Link:**
GoBack

**Subtitle:**
Register 19.9. UART_CONFO_REG (0x20)

**Body Text:**

Continued from the previous page...

- **UART_SW_DTR**: This register is used to configure the software DTR signal used in software flow control. (R/W)
  
- **UART_SW_RTS**: This bit is used in hardware flow control when UART_RX_FLOW_EN is 0. Set this bit to drive the RTS (or rts_out) signal low, and reset to drive the signal high. (R/W)

- **UART_STOP_BIT_NUM**: This register is used to set the length of the stop bit.
  - 0: Invalid. No effect
  - 1: 1 bit
  - 2: 1.5 bits
  - 3: 2 bits

(R/W)

- **UART_BIT_NUM**: This register is used to set the length of data; 0: 5 bits, 1: 6 bits, 2: 7 bits, 3: 8 bits.
  (R/W)

- **UART_PARITY_EN**: Set this bit to enable the UART parity check. (R/W)

- **UART_PARITY**: This register is used to configure the parity check mode; 0: even, 1: odd. (R/W)

**Footer:**
Espressif Systems
333 ESP32 TRM (Version 5.6)
Submit Documentation Feedback