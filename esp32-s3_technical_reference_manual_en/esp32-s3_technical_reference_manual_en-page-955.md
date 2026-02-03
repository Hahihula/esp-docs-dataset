**Title:**
Chapter 26 UART Controller (UART)

**GoBack Link:** [GoBack](#)

---

**Continued from previous page...**

- **Register: 26.6. UART_INT_CLR_REG (0x0010)**
  - **Field: UART_RS485_FRM_ERR_INTE_CLR**
    - Description: Set this bit to clear the UART_RS485_FRM_ERR_INTE interrupt.
    - Access Type: Write-Through
  - **Field: UART_RS485_CLASH_INTE_CLR**
    - Description: Set this bit to clear the UART_RS485_CLASH_INTE interrupt.
    - Access Type: Write-Through
  - **Field: UART_AT_CMD_CHAR_DET_INTE_CLR**
    - Description: Set this bit to clear the UART_AT_CMD_CHAR_DET_INTE interrupt.
    - Access Type: Write-Through

- **Register: 26.7. UART_CLKDIV_REG (0x0014)**
  - **Fields Overview**:
    - **UART_CLKDIV**: The integral part of the frequency divisor, accessible for read/write
    - **UART_CLKDIV_FRAG**: The fractional part of the frequency divisor, accessible for read/write

- **Register: 26.8. UART_RX_FILT_REG (0x0018)**
  - **Field: UART_GLITCH FILT**
    - Description: When input pulse width is lower than this value, the pulse is ignored.
    - Access Type: Read/Write
  - **Field: UART_GLITCH FILT_EN**
    - Description: Set this bit to enable RX signal filter.
    - Access Type: Read/Write

---

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version and Title: ESP32-S3 TRM (Version 1.7)
- Page Number: 955
- Submit Documentation Feedback Link [Submit Documentation Feedback](#)