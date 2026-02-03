**Title: Chapter 11 System Timer (SYSTIMER)**

---

### Register 11.17. SYSTIMER_COMP0_LOAD_REG (0x0050)

| Bit | Description |
|-----|-------------|
| 31-24 | Reserved |
| 0   | SYSTIMER_TIMER_COMP0_LOAD: COMPO synchronization enable signal. Set this bit to reload the alarm value/period to COMPO. (WT) |

---

### Register 11.18. SYSTIMER_TARGET1_HI_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31-20 | Reserved |
| 19   | SYSTIMER_TIMER_TARGET1_HI: The alarm value to be loaded to COMP1, high 20 bits. (R/W) |

---

### Register 11.19. SYSTIMER_TARGET1_LO_REG (0x0028)

| Bit | Description |
|-----|-------------|
| 31   | Reserved |
| 0    | SYSTIMER_TIMER_TARGET1_LO: The alarm value to be loaded to COMP1, low 32 bits. (R/W) |

---

**Footer:**  
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)

--- 

*Note: There is a "GoBack" link at the top right corner of the page.*