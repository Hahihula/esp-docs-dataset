**Title: Chapter 16 SHA Accelerator (SHA)**

---

### Register Information:

- **Register Name:** SHA_SHA1 BUSY  
  **Address:** 0x8C  
  **Description:** SHA-1 operation status.  
    - Value of `1` if the SHA accelerator is processing data, `0` if it is idle.
    - Access: Read-only (RO)

#### Diagram:
- A table with two columns labeled "31" and "0x00000000", showing a binary representation where both bits are set to 0.

---

### Register Information:

- **Register Name:** SHA_SHA256 START  
  **Address:** 0x90  
  **Description:** Start an SHA-256 operation on the first message block.
    - Value of `1` is required. 
    - Access: Write-only (WO)

#### Diagram:
- A table with two columns labeled "31" and "0x00000000", showing a binary representation where both bits are set to 0.

---

### Register Information:

- **Register Name:** SHA_SHA256 CONTINUE  
  **Address:** 0x94  
  **Description:** Continue the SHA-256 operation with subsequent blocks.
    - Value of `1` is required. 
    - Access: Write-only (WO)

#### Diagram:
- A table similar to previous, showing a binary representation where both bits are set to 0.

---

**Footer Information:**
- **Company:** Espressif Systems
- **Document Version:** ESP32 TRM (Version 5.6)
- **Page Number:** 298

**Link:** Submit Documentation Feedback