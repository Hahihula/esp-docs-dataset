**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.29. GPIO_STATUS_W1TC_REG (0x004C)

| Address | Value |
|---------|-------|
| 31      | 0     |

**Description:**  
GPIO_STATUS_W1TC GPIO0 ~ 31 interrupt status clear register. If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be cleared. Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT.

---

### Register 6.30. GPIO_STATUS1_WITS_REG (0x054)

| Address | Value |
|---------|-------|
| 31      | (reserved) |
| 22      | 0     |
| 21      | 0     |
| 20      | 0     |

**Description:**  
GPIO_STATUS_WITS GPIO32 ~ 48 interrupt status set register. If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS1_REG will be set to 1. Recommended operation: use this register to set GPIO_STATUS1_REG.

---

### Register 6.31. GPIO_STATUS1_W1TC_REG (0x058)

| Address | Value |
|---------|-------|
| 31      | (reserved) |
| 22      | 0     |
| 21      | 0     |
| 20      | 0     |

**Description:**  
GPIO_STATUS1_W1TC GPIO32 ~ 48 interrupt status clear register. If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS1_REG will be cleared. Recommended operation: use this register to clear GPIO_STATUS1_REG.

---

**Footer Information:**
- Espressif Systems
- Page number: 511
- Document version: ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback