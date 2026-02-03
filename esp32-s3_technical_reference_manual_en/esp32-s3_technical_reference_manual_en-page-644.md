**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** GoBack

---

**Section Header: Register 11.8. SYSTIMER_UNIT1_OP_REG (0x0008)**

- **Binary Representation Diagram**: Shows a binary number with bits labeled from right to left, starting at bit '31' and ending at bit '0'. The diagram is marked as "Reset" on the bottom.

**Description:**
SYSTIMER_TIMER_UNIT1_VALUE_VALID UNIT1 value is synchronized and valid. (R/SS/WTC)

**Binary Representation Description**: 
- **SYSTIMER_TIMER_UNIT1_UPDATE**: Update timer UNIT1, i.e., read the UNIT1 count value to SYS-TIMER_TIMER_UNIT1_VALUE_HI and SYSTIMER_TIMER_UNIT1_VALUE_LO. (WT)

---

**Section Header: Register 11.9. SYSTIMER_UNIT1_LOAD_HI_REG (0x0014)**

- **Binary Representation Diagram**: Similar binary number diagram as above, labeled "SYSTIMER UNIT1 LOAD HI" on the right.

**Description:**
SYSTIMER_TIMER_UNIT1_LOAD_HI The value to be loaded to UNIT1, high 20 bits. (R/W)

---

**Section Header: Register 11.10. SYSTIMER_UNIT1_LOAD_LO_REG (0x0018)**

- **Binary Representation Diagram**: Similar binary number diagram as above.

**Description:**
SYSTIMER_TIMER_UNIT1_LOAD_LO The value to be loaded to UNIT1, low 32 bits. (R/W)

---

**Footer Information:** 
Espressif Systems
644 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback