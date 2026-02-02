**Title:**
Chapter 19 UART Controller (UART)

**Subtitle:**
Register 19.3. UART_INT_ST_REG (0x8)

**Body Text with Descriptions of Register Bits and Interrupts:**

- **UART_AT_CMD_CHAR_DET_INT_ST**: The masked interrupt status bit for the UART_AT_CMD_CHAR_DET_INT interrupt.
  
- **UART_RS485_CLASH_INT_ST**: The masked interrupt status bit for the UART_RS485_CLASH_INT interrupt.

- **UART_RS485_FRM_ERR_INT_ST**: The masked interrupt status bit for the UART_RS485_FRM_ERR_INT interrupt.

- **UART_RS485_PARITY_ERR_INT_ST**: The masked interrupt status bit for the UART_RS485_PARITY_ERR_INT interrupt.

- **UART_TXDone_INT_ST**: The masked interrupt status bit for the UART_TX_DONE_INT interrupt.
  
- **UART_TX_BRK_IDLE DONE_INT_ST**: The masked interrupt status bit for the UART_TX_BRK_IDLEDONE_INT interrupt.
  
- **UART_TX_BRK_DONE_INT_ST**: The masked interrupt status bit for the UART_TX_BRK_DONE_INT interrupt.

- **UART_GLITCH_DET_INT_ST**: The masked interrupt status bit for the UART_GLITCH_DET_INT interrupt.
  
- **UART_SW_XOFF_INT_ST**: The masked interrupt status bit for the UART_SW_XOFF_INT interrupt.
  
- **UART_SW_XON_INT_ST**: The masked interrupt status bit for the UART_SW_XON_INT interrupt.

- **UART_RXFIFO_TOUT_INT_ST**: The masked interrupt status bit for the UART_RXFIFO_TOUT_INT interrupt.
  
- **UART_BRK_DET_INT_ST**: The masked interrupt status bit for the UART_BRK_DET_INT interrupt.
  
- **UART_CTS_CHG_INT_ST**: The masked interrupt status bit for the UART_CTS_CHG_INT interrupt.

- **UART_DSR_CHG_INT_ST**: The masked interrupt status bit for the UART_DSR_CHG_INT interrupt.

**Footer:**
Continued on the next page...

**Page Information at Bottom of Page:**
Espressif Systems
325 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Diagram Description in Image Content:**

The image contains a diagram that appears to be an address map or register layout for the UART controller, showing various interrupt status bits and their corresponding addresses within memory.

(Note: The exact structure of each bit is not fully visible due to resolution constraints.)