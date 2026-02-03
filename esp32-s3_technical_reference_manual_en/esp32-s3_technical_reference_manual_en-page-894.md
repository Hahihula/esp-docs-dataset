**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**GoBack Link:** GoBack

---

**Section Header and Register Information with Binary Representation:**

- **Register Name**: HMAC_SET_MESSAGE_END_REG (0x058)
  - **Binary Representation**: [Binary code here]
  
- **Register Name**: HMAC_SET_TEXT_END
  - Description: Set this bit to start hardware padding. (WO)

- **Register Name**: HMAC_SET_RESULT_FINISH_REG (0x05C)
  - **Binary Representation**: [Binary code here]

- **Register Name**: HMAC_SET_RESULT_END
  - Description: After read result from upstream, then let HMAC back to idle. (WO)

- **Register Name**: HMAC_SET_INVALIDATE_JTAG_REG (0x060)
  - **Binary Representation**: [Binary code here]
  
  - Description: Set this bit to clear calculation results when re-enabling JTAG in downstream mode. (WO)

---

**Footer Information:** 
Espressif Systems
894 ESP32-S3 TRM (Version 1.7) 

**Links:**
- Submit Documentation Feedback