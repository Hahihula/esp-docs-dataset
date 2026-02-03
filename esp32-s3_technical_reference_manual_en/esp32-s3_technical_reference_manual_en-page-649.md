**Title: Chapter 11 System Timer (SYSTIMER)**

---

**Register 11.23. SYSTIMER_TARGET2_LO_REG (0x0030)**
- **Description:** SYSTIMER_TIMER_TARGET2_LO. The alarm value to be loaded to COMP2, low 32 bits. (R/W)
- **Hexadecimal Value:** `0`

---

**Register 11.24. SYSTIMER_TARGET2_CONF_REG (0x003C)**
- **Description:**
  - SYSTIMER_TARGET2_TIMER_UNIT_SEL
    - **Field Description:** SYSIMER TARGET2 TIMER UNIT MODE
    - **Hexadecimal Value:** `0x0000`
  - SYSTIMER_TARGET2_PERIOD
    - **Field Description:** COMP2 alarm period. (R/W)
    - **Hexadecimal Value:** `0x0000`
  - SYSTIMER_TARGET2_PERIOD_MODE
    - **Description:** Set COMP2 to period mode. (R/W)
  - SYSTIMER_TARGET2_TIME_UNIT_SEL
    - **Description:** Select which counter unit to compare for COMP2. (R/W)

---

**Register 11.25. SYSTIMER_COMP2_LOAD_REG (0x0058)**
- **Hexadecimal Value:**
  - `0x0000`
- **Description:** SYSTIMER_TIMER_COMP2_LOAD. COMP2 synchronization enable signal. Set this bit to reload the alarm value/period to COMP2. (WT)

---

**Footer Information:**
- Page Number: "649"
- Document Version and Company Name:
  - ESP32-S3 TRM (Version 1.7)
  - Espressif Systems
- Link Texts:
  - Submit Documentation Feedback

--- 

(Note: The text in the image is structured as a technical document with register descriptions, hexadecimal values for each field within registers.)