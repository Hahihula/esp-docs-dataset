**Title: Chapter 19 UART Controller (UART)**

---

### Register 19.25. UART_MEM_RX_STATUS_REG (0x060)

| Field | Description |
|-------|-------------|
| 31    | (reserved) |
| 24-23 | (reserved) |
| 13, 12 | (reserved) |
| 2     | (reserved) |
| 1     | (reserved) |
| 0     | (reserved) |

| Bit | Description |
|-----|-------------|
| 0   | Reset |

- **UART_MEM_RX_RD_ADDR**  
  Represents the offset address to read RX FIFO. (RO)

- **UART_MEM_RX_WR_ADDR**  
  Represents the offset address to write RX FIFO. (RO)

---

### Register 19.26. UART_MEM_CNT_STATUS_REG (0x64)

| Field | Description |
|-------|-------------|
| 31    | (reserved) |
| ...   | ...         |

- **UART_TX_MEM_CNT**  
  Refer to the description of TXFIFO_CNT. (RO)

- **UART_RX_MEM_CNT**  
  Refer to the description of RXFIFO_CNT. (RO)

---

### Register 19.27. UARTPOSEPULSE_REG (0x68)

| Field | Description |
|-------|-------------|
| 31    | (reserved) |
| ...   | ...         |

- **UARTPOSEDGE_MIN_CNT**  
  This register stores the count of RxD positive edges. It is used in the autobaud detection process. (RO)

---

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback