**Title:**
Chapter 16 World Controller (WCL)

**Subtitles and Body Texts with Descriptions of Registers:**

- **Register 16.3. WCL_CORE_O_MESSAGE_ADDR_REG (0x0100)**
  - Diagram:
    ```
    +-------+---------+
    |       |         |
    |   31  |   0     |
    |       |         |
    +-------+---------+
    ```
  - Description: 
    WCL_CORE_O_MESSAGE_ADDR Configures the address to write agreed sequence to clear write_buffer for CPUO. (R/W)

- **Register 16.4. WCL_CORE_O_MESSAGE_MAX_REG (0x0104)**
  - Diagram:
    ```
    +-------+---------+
    |       |         |
    |   31  |   4     |
    |       |         |
    +-------+---------+
    ```
  - Description: 
    WCL_CORE_O_MESSAGE_MAX Configures the agreed sequence to write to clear write_buffer for CPUO. It’s advised to set this field to no less than 3. (R/W)

**Footer Information:**
- Company Name:
  Espressif Systems
- Document Version and Type:
  ESP32-S3 TRM (Version 1.7)
- Page Number:
  815

**Navigation Links:**
- GoBack