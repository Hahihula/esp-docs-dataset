**Chapter Title:**
Chapter 15 RSA Accelerator (RSA)

**GoBack Link:** GoBack

---

**Register Section:**

- **Register Name and Address:**
  - Register 15.4. RSA_MULT_MODE_REG (0x80C)
  
  **Description of the register contents:**
  - `RSAMultMode` This register contains the mode of modular multiplication and multiplication.
  - Access type is `(R/W)`

- **Register Name and Address:**
  - Register 15.5. RSA_MULT_START_REG (0x810)
  
  **Description of the register contents:**
  - `RSA_mult_start` Write 1 to start modular multiplication or multiplication.
  - Access type is `(WO)`
  - Reset value indicated.

- **Register Name and Address:**
  - Register 15.6. RSA_INTERRUPT_REG (0x814)
  
  **Description of the register contents:**
  - `RSA_interrupt` RSA interrupt status register. Will read 1 once an operation has completed.
  - Access type is `(R/W)`
  - Reset value indicated.

- **Register Name and Address:**
  - Register 15.7. RSA_CLEAN_REG (0x818)
  
  **Description of the register contents:**
  - `RSA_clean` This bit will read 1 once the memory initialization is completed.
  - Access type is `(RO)`
  - Reset value indicated.

---

**Footer Information:** 
- Page number and document version:
  - "292 ESP32 TRM (Version 5.6)"
  
- Company information: Espressif Systems
  
- Link for submitting documentation feedback:
  - Submit Documentation Feedback

--- 

The image also contains binary representations of the registers, but they are not transcribed here as per your instructions to preserve only text content and avoid conversational elements or descriptions that go beyond what is visible.