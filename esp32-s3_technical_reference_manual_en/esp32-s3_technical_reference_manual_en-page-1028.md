**Title: Chapter 27 I2C Controller (I2C)**

**Subtitle: Register 27.20. I2C_FIFO_ST_REG (0x0014)**

- **Field:** `I2C_SLAVE_RW POINT`
- **Field:** `I2C_TXFIFO_WADDR`
- **Field:** `I2C_RXFIFO_RADDR`

**Table:**
| 31 | 30 | 29 | ... | reserved | (reserved) |
|----|----|----|-----|----------|-------------|
| O  |   |   |     |          |             |

- **Field Description:** `I2C_RXFIFO_RADDR` - This is the offset address of APB reading from RX FIFO. (RO)
- **Field Description:** `I2C_TXFIFO_RADDR` - This is the offset address of I2C controller reading from TX FIFO. (RO)

**Table:**
| 31 | ... |
|----|-----|
| O  |     |

- **Field Description:** `I2C_TXFIFO_WADDR` - This is the offset address of APB bus writing to TX FIFO. (RO)
- **Field Description:** `I2C_SLAVE_RW POINT` - The received data in I2C slave mode. (RO)

**Subtitle: Register 27.21. I2C_DATA_REG (0x001C)**

- **Field:** `I2C_FIFO_RDATA`
  
**Table:**
| 31 | ... |
|----|-----|
| O  |     |

- **Field Description:** `I2C_FIFO_RDATA` - This field is used to read data from RX FIFO, or write data to TX FIFO. (R/W)

---

*Footer:* Espressif Systems  
Page number: 1028  
Document version: ESP32-S3 TRM (Version 1.7)  

**Link:** Submit Documentation Feedback