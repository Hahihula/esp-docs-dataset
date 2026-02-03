**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**GoBack Link:** GoBack

---

**Section Header:**
Register 21.10. HMAC_SET_INVALIDATE_DS_REG (0x064)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from right to left.
- Description:
  - **HMAC_SET_INVALIDATE_DS_S:** Set this bit to clear calculation results of the DS module in downstream mode.

---

**Section Header:**
Register 21.11. HMAC QUERY ERROR REG (0x68)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from right to left.
- Description:
  - **HMAC_QUERY_CHECK:** Indicates whether a HMAC key matches the purpose.

---

**Subsection Header:**
- O: HMAC key and purpose match
- I: error (RO)

---

**Section Header:**
Register 21.12. HMAC_QUERY BUSY REG (0x6C)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from right to left.
- Description:
  - **HMAC_BUSY_STATE:** Indicates whether HMAC is in busy state.

---

**Subsection Header:**
- I'80: idle
- I'81: HMAC is still working for calculation. (RO)

---

**Footer Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback