**Title: Chapter 20 RSA Accelerator (RSA)**

---

### Register 20.5. RSA_MODMULT_START_REG (0x810)

- **Field:** `0` to `31`
- **Description:** 
  - **Name:** RSA_MODMULT_START
  - **Function:** Set this bit to 1 to start the modular multiplication.
  - **Access Mode:** WO

---

### Register 20.6. RSA_MULT_START_REG (0x814)

- **Field:** `0` to `31`
- **Description:**
  - **Name:** RSAMultStart
  - **Function:** Set this bit to 1 to start the multiplication.
  - **Access Mode:** WO

---

### Register 20.7. RSA_IDLE_REG (0x818)

- **Field:** `0` to `31`
- **Description:**
  - **Name:** RSAIdle
  - **Function:** The content of this bit is 1 when the RSA accelerator is idle.
  - **Access Mode:** RO

---

### Register 20.8. RSA_CLEAR_INTERRUPT_REG (0x81C)

- **Field:** `0` to `31`
- **Description:**
  - **Name:** RSAClearInterrupt
  - **Function:** Set this bit to 1 to clear the RSA interrupts.
  - **Access Mode:** WO

---

**Footer Information:**

- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 880
- Links:
  - Submit Documentation Feedback