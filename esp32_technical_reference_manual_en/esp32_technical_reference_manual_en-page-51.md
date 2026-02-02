**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**GoBack Link:** GoBack

---

**Section Header:**
Register 1.10. RTC_I2C_DEBUG_STATUS_REG (0x08)

**Table Description for Register 1.10:**
- **Field Name**: RTC_I2C_SCL_STATE
  - **Description**: State of SCL machine.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C_MAIN_STATE
  - **Description**: State of the main machine.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C_BYTETrans
  - **Description**: 8-bit transmit done.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C_SLAVE_ADDR_MATCH
  - **Description**: Indicates whether the addresses are matched, when in slave mode.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C BUS BUSY
  - **Description**: Operation is in progress.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C_ARB_LOST
  - **Description**: Indicates the loss of I2C bus control, when in master mode.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C_TIMED_OUT
  - **Description**: Transfer has timed out.
  - **Access Mode**: Read/Write

- **Field Name**: RTC_I2C_SLAVE_RW
  - **Description**: Indicates the value of the received R/W bit, when in slave mode.

- **Field Name**: RTC_I2C_ACK_VAL
  - **Description**: The value of ACK signal on the bus.
  - **Access Mode**: Read/Write

**Binary Representation for Register 1.10:**
```
31 30 28 27 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
| RTC_I2C_SCL_STATE | RTC_I2C_MAIN_STATE | RTC_I2C_BYTETrans | ... | RTC_I2C_ACK_VAL |
```

---

**Section Header:**
Register 1.11. RTC_I2C_TIMEOUT_REG (0x00c)

**Table Description for Register 1.11:**
- **Field Name**: RTC_I2C_TIMEOUT
  - **Description**: Maximum number of RTC_FAST_CLK cycles that the transmission can take.
  - **Access Mode**: Read/Write

**Binary Representation for Register 1.11:**
```
31 30 28 27 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0
| RTC_I2C_TIMEOUT |
```

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)