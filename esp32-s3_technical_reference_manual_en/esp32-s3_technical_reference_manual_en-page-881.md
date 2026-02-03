**Chapter Title:**
Chapter 20 RSA Accelerator (RSA)

**GoBack Link:** GoBack

---

**Register Section:**

- **Register Name and Address:**
  - Register 20.9. RSA_CONSTANT_TIME_REG (0x0820)
  
- **Field Description for RSA_CONSTANT_TIME_REG:**
  - **Name:** RSA_CONSTANT_TIME_REG
  - **Description:** Controls the constant_time option.
    - **Options:** 
      - `0`: acceleration by default.
      - `1`: no acceleration

- **Register Name and Address:**
  - Register 20.10. RSA_SEARCH_ENABLE_REG (0x0824)
  
- **Field Description for RSA_SEARCH_ENABLE_REG:**
  - **Name:** RSA_SEARCH_ENABLE_REG
  - **Description:** Controls the search option.
    - **Options:** 
      - `0`: no acceleration by default.
      - `1`: acceleration

- **Register Name and Address:**
  - Register 20.11. RSA_SEARCH_POS_REG (0x0828)
  
- **Field Description for RSA_SEARCH_POS_REG:**
  - **Name:** RSA_SEARCH_POS
  - **Description:** Is used to configure the starting address when the acceleration option of search is used.

---

**Footer Information:**

- Company Name and Document Version:
  - Espressif Systems, ESP32-S3 TRM (Version 1.7)
  
- Submit Documentation Feedback Link:

--- 

**Binary Representation Diagrams for Each Register:** 
Each register section includes a binary representation diagram showing the bit positions with labels indicating their names or purposes.

**Note:**
The exact structure of each field in terms of bits is not fully detailed here, but it's represented visually as per standard documentation conventions.