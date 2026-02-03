**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.26. GPIO_CPU_INT1_REG (0x0068)

| Offset | Description |
|--------|-------------|
| 31     | reserved    |
| 22-21 | GPIO_CPU_INT1 | 
| 0      | Reset       |

GPIO_CPU1_INT GPIO32 ~ 48 CPU interrupt status. This interrupt status is corresponding to the bit in GPIO_STATUS1_REG when assert (high) enable signal (bit 13 of GPIO_PINn_REG). (RO)

---

### Register 6.27. GPIO_CPU_NMI_INT1_REG (0x006C)

| Offset | Description |
|--------|-------------|
| 31     | reserved    |
| 22-21 | GPIO_CPU_NMI1 | 
| 0      | Reset       |

GPIO_CPU_NMI1_INT GPIO32 ~ 48 CPU non-maskable interrupt status. This interrupt status is corresponding to bit in GPIO_STATUS1_REG when assert (high) enable signal (bit 14 of GPIO_PINn_REG). (RO)

---

### Register 6.28. GPIO_STATUS_W1TS_REG (0x0048)

| Offset | Description |
|--------|-------------|
| 31     | reserved    |
| 0      | Reset       |

GPIO_STATUS_W1TS GPIO0 ~ 31 interrupt status set register. If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be set to 1. Recommended operation: use this register to set GPIO_STATUS_INTERRUPT. (WO)

---

**Footer:**  
Espressif Systems  
510  
ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback