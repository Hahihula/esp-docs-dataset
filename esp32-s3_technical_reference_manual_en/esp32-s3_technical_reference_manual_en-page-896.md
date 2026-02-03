**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**GoBack Link:** GoBack

---

**Section Header and Description with Register Information:**

- **Register Name**: HMAC_WR_MESSAGE_n_REG  
  - **Description**: Store the nth 32-bit of message. (WO)  
  - **Address Range**: n : 0-15 (0x080+4*n)
  - **Example Value**: 0

**Field within Register:**
- **Field Name**: HMAC_WDATA_n
  - **Description**: Store the nth 32-bit of message. (WO)

---

**Section Header and Description with Register Information:**

- **Register Name**: HMAC_RD_RESULT_n_REG  
  - **Description**: Read the nth 32-bit of hash result. (RO)  
  - **Address Range**: n : 0-7 (0xC0+4*n)
  - **Example Value**: 0

**Field within Register:**
- **Field Name**: HMAC_RDATA_n
  - **Description**: Read the nth 32-bit of hash result. (RO)

---

**Section Header and Description with Register Information:**

- **Register Name**: HMAC_SET_MESSAGE_PAD_REG  
  - **Address Range**: 0x0F0

**Field within Register:**
- **Field Name**: HMAC_SET_TEXT_PAD
  - **Description**: Set this bit to start software padding. (WO)

---

**Section Header and Description with Register Information:**

- **Register Name**: HMAC_ONE_BLOCK_REG  
  - **Address Range**: 0x0F4

**Field within Register:**
- **Field Name**: HMAC_SET_ONE_BLOCK
  - **Description**: Set this bit to show that no padding is required. (WO)

---

**Footer with Document Information and Feedback Link:**

Espressif Systems  
896 ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)