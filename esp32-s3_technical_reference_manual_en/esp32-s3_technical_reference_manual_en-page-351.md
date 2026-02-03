**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section Header:**
GoBack

**Register Information Section:**

- **Title:** Register 2.28. RTC_I2C_CMDO_REG (0x0038)
  - **Field Description:**
    - `RTC_I2C_COMMANDO_DONE`
      - **Content of command O. For more information, please refer to the register I2C COMMANDO REG in Chapter I2C Controller. (R/W)**
      - **RTC_I2C_COMMANDO DONE** When command 0 is done, this bit changes to 1. (RO)
    - **Binary Representation:** 
      ```
      31 30     14 13       0
      0 0 0 0   0 0 0 0    0x903 Reset
      ```

- **Title:** Register 2.29. RTC_I2C_CMD1_REG (0x003C)
  - **Field Description:**
    - `RTC_I2C_COMMAND1`
      - **Content of command 1. For more information, please refer to the register I2C COMMAND1 REG in Chapter I2C Controller. (R/W)**
      - **RTC_I2C_COMMAND1 DONE** When command 1 is done, this bit changes to 1. (RO)
    - **Binary Representation:** 
      ```
      31 30     14 13       0
      0 0 0 0   0 0 0 0    0x901 Reset
      ```

- **Title:** Register 2.30. RTC_I2C_CMD2_REG (0x0040)
  - **Field Description:**
    - `RTC_I2C_COMMAND2`
      - **Content of command 2. For more information, please refer to the register I2C COMMAND2 REG in Chapter I2C Controller. (R/W)**
      - **RTC_I2C_COMMAND2 DONE** When command 2 is done, this bit changes to 1. (RO)
    - **Binary Representation:** 
      ```
      31 30     14 13       0
      0 0 0 0   0 0 0 0    0x902 Reset
      ```

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)