**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**GoBack**

**Register 2.11. SENS_SAR_SLAVE_ADDR2_REG (0x044)**
- **Binary representation:** 
  ```
  31    22   21     11    10      9       8       7       6       5       4       3       2       1       0
  (reserved) SENS_I2C_SLAVE_ADDR2 SENS_I2C_SLAVE_ADDR2 RESET
  ```
- **Description:**
  - `SENS_I2C_SLAVE_ADDR3` RTC I2C slave address 3. (R/W)
  - `SENS_I2C_SLAVE_ADDR2` RTC I2C slave address 2. (R/W)

**Register 2.12. SENS_SAR_SLAVE_ADDR3_REG (0x048)**
- **Binary representation:** 
  ```
  31    22   21     11    10      9       8       7       6       5       4       3       2       1       0
  (reserved) SENS_I2C_SLAVE_ADDR3 SENS_I2C_SLAVE_ADDR3 RESET
  ```
- **Description:**
  - `SENS_I2C_SLAVE_ADDR5` RTC I2C slave address 5. (R/W)
  - `SENS_I2C_SLAVE_ADDR4` RTC I2C slave address 4. (R/W)

**Register 2.13. SENS_SAR_SLAVE_ADDR4_REG (0x04C)**
- **Binary representation:** 
  ```
  31    22   21     11    10      9       8       7       6       5       4       3       2       1       0
  (reserved) SENS_I2C_SLAVE_ADDR4 SENS_I2C_SLAVE_ADDR4 RESET
  ```
- **Description:**
  - `SENS_I2C_SLAVE_ADDR7` RTC I2C slave address 7. (R/W)
  - `SENS_I2C_SLAVE_ADDR6` RTC I2C slave address 6. (R/W)

**Section Title: 2.10.4 RTC I2C (I2C) Registers**
- **Description:** The addresses in this section are relative to low-power management base address + 0x0C00 provided in Table 4.3-3 in Chapter 4 System and Memory.

**Footer Information:**
- Page number: 342
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Link:** Submit Documentation Feedback