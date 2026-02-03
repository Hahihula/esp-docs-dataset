**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

### Register 6.23. GPIO_STATUS1_REG (0x0050)

| Bit | Description |
|-----|-------------|
| 31-24 | Reserved |
| 23   | GPIO_STATUS1INTERRUPT |
| 22   | Reserved |
| 21   | Reserved |
| 20   | Reserved |
| ...  | ...         |
| 0    | Reset       |

**Description:**  
GPIO_STATUS1_INTERRUPT GPIO32 ~ 48 interrupt status register. (R/W)

---

### Register 6.24. GPIO_CPU_INT_REG (0x005C)

| Bit | Description |
|-----|-------------|
| 31   | Reserved    |
| ...  | ...         |
| 0    | Reset       |

**Description:**  
GPIO_CPU_INT GPIO0 ~ 31 CPU interrupt status. This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit13 of GPIO_PINn_REG). (RO)

---

### Register 6.25. GPIO_CPU_NMI_INT_REG (0x0060)

| Bit | Description |
|-----|-------------|
| 31   | Reserved    |
| ...  | ...         |
| 0    | Reset       |

**Description:**  
GPIO_CPU_NMI_INT GPIO0 ~ 31 CPU non-maskable interrupt status. This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit 14 of GPIO_PINn_REG). (RO)

---

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)
Page number at bottom center, which is not specified but can be inferred from the context as part of a larger document or manual.

(Note: The exact content and structure may vary slightly based on how this image was captured.)