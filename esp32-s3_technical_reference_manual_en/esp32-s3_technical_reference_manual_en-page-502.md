**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.3. GPIO_OUT_WITS_REG (0x0008)

| **Field Name** | **Value Range** |
|-----------------|------------------|
| GPIO_OUT_WITS   | 0x000000          |

**Description:**
GPIO_OUT_WITS ~ 31 output set register. If the value 1 is written to a bit here, the corresponding bit in GPIO_OUT_REG will be set to 1. Recommended operation: use this register to set GPIO_OUT_REG.

---

### Register 6.4. GPIO_OUT_WITC_REG (0x000C)

| **Field Name** | **Value Range** |
|-----------------|------------------|
| GPIO_OUT_WITC   | 0x000000          |

**Description:**
GPIO_OUT_WITC ~ 31 output clear register. If the value 1 is written to a bit here, the corresponding bit in GPIO_OUT_REG will be cleared. Recommended operation: use this register to clear GPIO_OUT_REG.

---

### Register 6.5. GPIO_OUT1_REG (0x0010)

| **Field Name** | **Value Range** |
|-----------------|------------------|
| GPIO_OUT1_DATA_ORIG | 0x0000          |

**Description:**
GPIO_OUT1_DATA_ORIG ~ GPIO32 ~ 48 output value in simple GPIO output mode. The values of bit0 ~ bit16 correspond to GPIO32 ~ GPIO48. Bit17 ~ bit21 are invalid.

---

**Footer Information:**  
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)