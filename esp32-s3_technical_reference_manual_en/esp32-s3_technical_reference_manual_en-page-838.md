**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**GoBack Link:** GoBack

**Register Information for SYSTEM_CACHE_CONTROL_REG (0x0048):**

- **Register Name and Address:** Register 17.15. SYSTEM_CACHE_CONTROL_REG (0x0048)
- **Bit Description:**
  - `SYSTEM_ICACHE_CLK_ON`: Set this bit to enable i-cache clock.
    - Access Type: Read/Write
  - `SYSTEM_ICACHE_RESET`: Set this bit to reset i-cache.
    - Access Type: Read/Write
  - `SYSTEM_DCACHE_CLK_ON`: Set this bit to enable d-cache clock.
    - Access Type: Read/Write
  - `SYSTEM_DCACHE_RESET`: Set this bit to reset d-cache.
    - Access Type: Read/Write

**Bit Layout Diagram:** [Binary layout diagram showing the positions of each function]

---

**Register Information for SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG (0x004C):**

- **Register Name and Address:** Register 17.16. SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG (0x004C)
- **Bit Description:**
  - `SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT`: Set this bit to enable Manual Encryption under SPI Boot mode.
    - Access Type: Read/Write
  - `SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT`: Set this bit to enable Auto Encryption under Download Boot mode.
    - Access Type: Read/Write
  - `SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT`: Set this bit to enable Auto Decryption under Download Boot mode.
    - Access Type: Read/Write
  - `SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT`: Set this bit to enable Manual Encryption under Download Boot mode.
    - Access Type: Read/Write

**Bit Layout Diagram:** [Binary layout diagram showing the positions of each function]

---

**Footer Information:**
- Page Number: 838
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name and Link for Feedback:
  - Espressif Systems
  - Submit Documentation Feedback

(Note: The binary layout diagrams are not described in text form as they require visual interpretation.)