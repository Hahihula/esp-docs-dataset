**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**GoBack**

**Section Header:**
Register 2.20. RTC_I2C_STATUS_REG (0x0008)

**Binary Register Description with Labels and Values:**
- **Field Name:** RTC_I2C_ACK_REC
  - **Description:** The received ACK value.
  - **Values:** 
    - `0`: ACK
    - `1`: NACK. (RO)
  
- **Field Name:** RTC_I2C_SLAVE_RW
  - **Description:** When the master writes to slave; when the master reads from slave.
  - **Values:**
    - `0`: Master writes to slave;
    - `1`: Master reads from slave. (RO)

- **Field Name:** RTC_I2C_ARB_LOST
  - **Description:** When the RTC I2C loses control of SCL line, the register changes to 1.
  - **Values:**
    - `0`: No loss;
    - `1`: Loss occurs when master writes or reads from slave. (RO)

- **Field Name:** RTC_I2C BUS BUSY
  - **Description:** When the I2C bus is idle state; when the I2C bus is busy transferring data.
  - **Values:**
    - `0`: Idle;
    - `1`: Busy transfer in progress. (RO)

- **Field Name:** RTC_I2C_SLAVE_ADDRESSED
  - **Description:** When the address sent by master matches with slave's address, this bit will be set to indicate that a valid I2C transaction is taking place.
  - **Values:**
    - `0`: No match;
    - `1`: Match found. (RO)

- **Field Name:** RTC_I2C_BYTETrans
  - **Description:** This field changes to 1 when one byte transfer occurs in the data bus during an I2C transaction, indicating that a valid address has been received.
  - **Values:**
    - `0`: No bytes transferred;
    - `1`: One byte is being transmitted. (RO)

- **Field Name:** RTC_I2C_OP_CNT
  - **Description:** Indicates which operation the register supports.

**Section Header:**
Register 2.21. RTC_I2C_TIMEOUT_REG (0x000C)

**Binary Register Description with Labels and Values:**
- **Field Name:** RTC_I2C_TIMEOUT
  - **Description:** Timeout threshold.
  - **Values:**
    - `0`: No timeout;
    - `1`: Set to indicate a specific time out value. (R/W)

**Section Header:**
Register 2.22. RTC_I2C_SLAVE_ADDR_REG (0x0010)

**Binary Register Description with Labels and Values:**
- **Field Name:** RTC_I2C_ADDR_10BIT_EN
  - **Description:** This field is used to enable the slave's 10-bit addressing mode.
  - **Values:**
    - `0`: Disabled;
    - `1`: Enabled. (R/W)

**Footer Information:**
Espressif Systems  
346 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback