**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**GoBack Link:** GoBack

---

**Section Header: Register 23.4. XTS_AES_PHYSICAL_ADDRESS_REG (0x0048)**

- **Field Description:**
  - **Name:** XTS_AES_PHYSICAL_ADDRESS
  - **Type:** Physical address.
  - **Access Mode:** Read/Write
  
- **Bitfield Table:**
  - **Bits 31, 30, and 29** are reserved (not shown in the image).
  - **Bits 0 to 0x00000000**: Reset value is provided.

---

**Section Header: Register 23.5. XTS_AES_TRIGGER_REG (0x004C)**

- **Field Description:**
  - **Name:** XTS_AESTrigger
  - **Type:** Write to enable manual encryption.
  
- **Bitfield Table:**
  - **Bits 31** is reserved and not shown in the image.

---

**Section Header: Register 23.6. XTS_AES_RELEASE_REG (0x0050)**

- **Field Description:**
  - **Name:** XTS_AESRelease
  - **Type:** Write to grant SPI1 access to encrypted result.
  
- **Bitfield Table:**
  - **Bits 31** is reserved and not shown in the image.

---

**Section Header: Register 23.7. XTS_AES_DESTROY_REG (0x0054)**

- **Field Description:**
  - **Name:** XTS_AESDestroy
  - **Type:** Write to destroy encrypted result.
  
- **Bitfield Table:**
  - **Bits 31** is reserved and not shown in the image.

---

**Footer Information:**
- Company Name: Espressif Systems
- Document Version: ESP32-S3 TRM (Version 1.7)
- Page Number: 917

**Link:** Submit Documentation Feedback