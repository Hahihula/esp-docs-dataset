**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Section Header:**
GoBack

**Register Information and Description:**

- **Register Name:** Register 21.15, I2C_SCL_START_HOLD_REG (0x0040)
  - **Description:** This register is used to configure the time between the negative edge of SDA and the negative edge of SCL for a START condition in APB clock cycles.
  - **Access Type:** Read/Write
  - **Bit Description:**
    ```
    31  9   0
    (reserved) Reset
    ```

- **Register Name:** Register 21.16, I2C_SCL_RSTART_SETUP_REG (0x0044)
  - **Description:** This register is used to configure the time between the positive edge of SCL and the negative edge of SDA for a RESTART condition in APB clock cycles.
  - **Access Type:** Read/Write
  - **Bit Description:**
    ```
    31   9   0 (reserved) Reset
    ```

- **Register Name:** Register 21.17, I2C_SCL_STOP_HOLD_REG (0x0048)
  - **Description:** This register is used to configure the delay after the STOP condition in APB clock cycles.
  - **Access Type:** Read/Write
  - **Bit Description:**
    ```
    31   14  13  9 (reserved) Reset
    ```

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Title: ESP32 TRM (Version 5.6)
- Page Number: 412

**Action Links:** 
- Submit Documentation Feedback