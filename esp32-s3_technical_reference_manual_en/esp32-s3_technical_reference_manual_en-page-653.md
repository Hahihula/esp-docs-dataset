**Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** [GoBack](#)

---

**Section Title: Register 11.34. SYSTIMER_REAL_TARGET2_LO_REG (0x0084)**

- **Description:** 
  - `SYSTIMER TARGET2_LO_RO` Actual target value of COMP2, low 32 bits.
  
- **Register Address and Description in Diagram Form:**
  ```markdown
  31    0
  SYSTIMER_TARGET2_LO_RO
  ```

**Section Title: Register 11.35. SYSTIMER_REAL_TARGET2_HI_REG (0x0088)**

- **Description:** 
  - `SYSTIMER TARGET2_HI_RO` Actual target value of COMP2, high 20 bits.

- **Register Address and Description in Diagram Form:**
  ```markdown
  31    0   20  19  0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
  SYSTIMER_TARGET2_HI_RO
  ```

**Section Title: Register 11.36. SYSTIMER_DATE_REG (0x00FC)**

- **Description:** 
  - `SYSTIMER_DATE` Version control register.

- **Register Address and Description in Diagram Form:**
  ```markdown
  31    0   0x2012251
  SYSTIMER_DATE
  ```

---

**Footer Information:**
- Page Number: 653
- Company Name: Espressif Systems
- Document Title and Version Info:
  - ESP32-S3 TRM (Version 1.7)
- Link for Submitting Documentation Feedback: [Submit Documentation Feedback](#)