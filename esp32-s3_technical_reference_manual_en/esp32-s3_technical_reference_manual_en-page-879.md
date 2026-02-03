**Title:**
Chapter 20 RSA Accelerator (RSA)

**Menu:**
GoBack

---

**Section Title: Register 20.1. RSA_M_PRIME_REG (0x0800)**
- **Field Name:** RSA_M_PRIME_REG
- **Description:** Stores M' (R/W)
- **Hexadecimal Value:** 0x00000000

---

**Section Title: Register 20.2. RSA_MODE_REG (0x0804)**
- **Field Name:** RSA_MODE
- **Description:** Stores the mode of modular exponentiation. (R/W)
- **Hexadecimal Value Representation:** 
  - Reset value shown as a series of zeros and ones.
  
---

**Section Title: Register 20.3. RSA_CLEAN_REG (0x0808)**
- **Field Name:** RSA_CLEAN
- **Description:** The content of this bit is 1 when memories complete initialization. (RO)
- **Hexadecimal Value Representation:** 
  - Reset value shown as a series of zeros and ones.

---

**Section Title: Register 20.4. RSA_MODEXP_START_REG (0x080C)**
- **Field Name:** RSA_MODEXP_START
- **Description:** Set this bit to 1 to start the modular exponentiation. (WO)
- **Hexadecimal Value Representation:** 
  - Reset value shown as a series of zeros and ones.

---

**Footer:**
Espressif Systems  
879 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback