**Title: Chapter 26 UART Controller (UART)**

---

Continued from the previous page...

- **Register 26.9. UART_CONF0_REG (0x0020)**
  - **UART_TXD_INV**: Set this bit to invert the level value of UART TXD signal.
    - Access: Read/Write
  - **UART_RTS_INV**: Set this bit to invert the level value of UART RTS signal.
    - Access: Read/Write
  - **UART_DTR INV**: Set this bit to invert the level value of UART DTR signal.
    - Access: Read/Write

- **Register 26.10. UART_CONF1_REG (0x0024)**
  - **UART_CLK_EN**:
    - Description: O: Support clock only when application writes registers; R: Force clock on for registers
      - Access: Read/Write
  
  - **UART_ERR_WR_MASK**: Receiver stores the data even if the received data is wrong; 1: Receiver stops storing data into FIFO when data is wrong.
    - Access: Read/Write

  - **UART_AUTOBAUD_EN**: This is the enable bit for baud rate detection. 
    - Access: Read/Write
  
  - **UART_MEM_CLK_EN**: The signal to enable UART RAM clock gating
    - Access: Read/Write

---

**Register 26.10. UART_CONF1_REG (0x0024)**
- **Field Descriptions and Values**

| Field Name | Description | Value |
|-------------|-------------|-------|
| 31         | Reserved     |      |
| 24         | UART_RX Flow Direction |       |
| 23         | UART_RX Flow Data Out Overflow |    |
| 22         | UART_RX Flow Data In Overflow |   |
| 21         | UART_RX Flow Data In Overflow |   |
| 20         | UART_RX Flow Data In Overflow |   |
| 19         | UART_RX Flow Data In Overflow |   |
| 18         | UART_RX Flow Data In Overflow |   |
| 17         | UART_RX Flow Data In Overflow |   |
| 16         | UART_RX Flow Data In Overflow |   |
| 15         | UART_RX Flow Data In Overflow |   |
| 14         | UART_RX Flow Data In Overflow |   |
| 13         | UART_RX Flow Data In Overflow |   |
| 12         | UART_RX Flow Data In Overflow |   |
| 11         | UART_RX Flow Data In Overflow |   |
| 10         | UART_RX Flow Data In Overflow |   |
| 9          | UART_RX Flow Data In Overflow |   |
| 8          | UART_RX Flow Data In Overflow |   |
| 7          | UART_RX Flow Data In Overflow |   |
| 6          | UART_RX Flow Data In Overflow |   |
| 5          | UART_RX Flow Data In Overflow |   |
| 4          | UART_RX Flow Data In Overflow |   |
| 3          | UART_RX Flow Data In Overflow |   |
| 2          | UART_RX Flow Data In Overflow |   |
| 1          | UART_RX Flow Data In Overflow |   |
| 0          | UART_RX Flow Data In Overflow |   |

---

**Field Descriptions and Values**

- **UART_RX_FIFO_FULL_THRD**: An UART_RX_FIFO_FULL_INT interrupt is generated when the receiver receives more data than the value of this field.
  - Access: Read/Write
  
- **UART_TX_FIFO_EMPTY_THRD**: An UART_TX_FIFO_EMPTY_INT interrupt is generated when the number of data bytes in TX FIFO is less than the value of this field. 
  - Access: Read/Write

- **UART_DIS_RX_DAT_OVF**: Disable UART RX data overflow detection.
  - Access: Read/Write
  
- **UART_RX_TOUT_FLOWDis**: Set this bit to stop accumulating idle_cnt when hardware flow control works
  - Access: Read/Write
  
- **UART_RX_FLOW_EN**: This is the flow enable bit for UART receiver. 
  - Access: Read/Write
  
- **UART_RX_TOUT_EN**: This is the enable bit for UART receiver’s timeout function.
  - Access: Read/Write

---

**Footer Information**
- Page Number: 957
- Document Version: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems
- Link Texts:
  - Submit Documentation Feedback