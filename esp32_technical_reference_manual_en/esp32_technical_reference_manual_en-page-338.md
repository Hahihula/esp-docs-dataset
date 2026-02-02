**Chapter Title:**
Chapter 19 UART Controller (UART)

**Section Header:**
Register 19.18. UART_RS485_CONF_REG (0x44)

**Table Description:**
- The table shows the bit layout of the UART_RS485_CONF_REG register.
- Bits are labeled from right to left, starting with "Reset" and ending at "UART_RS485_TX_DLY_NUM".

**Register Descriptions:**

1. **UART_RS485_TX_DLY_NUM**
   - Description:
     This register is used to delay the transmitter’s internal data signal.
   - Access Type (R/W)

2. **UART_RS485_RX_DLY_NUM**
   - Description:
     This register is used to delay the receiver's internal data signal.
   - Access Type (R/W)

3. **UART_RS485RXBY_TX_EN 1:**
   - Description:
     enable the RS-485 transmitter to send data, when the RS-485 receiver line is busy; 0: the RS-485 transmitter should not send data, when its receiver is busy.
   - Access Type (R/W)

4. **UART_RS485TX_RX_EN**
   - Description:
     Set this bit to enable the transmitter’s output signal loop back to the receiver’s input signal.
   - Access Type (R/W)

5. **UART_DL1_EN**
   - Description:
     Set this bit by delay the STOP bit by 1 bit after DL1.
   - Access Type (R/W)

6. **UART_DLO_EN**
   - Description:
     Set this bit to choose the RS-485 mode.

**Register Descriptions Continued:**

7. **Register 19.19. UART_AT_CMD_PRECNT_REG (0x48)**
   - The table shows a similar layout as above, but with different bits labeled from right to left.
   - Bits are not explicitly described in the provided text snippet.

**Additional Information about Register:**

- **UART_PRE_IDLE_NUM**
  - Description:
    This register is used to configure the idle-time duration before the first `at_cmd` is received by the receiver. When the duration is less than what this register indicates, it will not take the next data received as an at_cmd char.
  - Access Type (R/W)

**Footer:**
- Page number and document version information:
  "338 ESP32 TRM (Version 5.6)"
  
- Company name:
  Espressif Systems

- Links for additional actions or feedback:
  Submit Documentation Feedback