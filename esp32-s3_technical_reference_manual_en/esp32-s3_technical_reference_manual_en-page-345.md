**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**GoBack**

---

**Register Description:**  
RTC_I2C_CTRL_REG (0x0004)

| Bit Number | Name                          |
|------------|-------------------------------|
| 31         | RTC_I2C_RESET                |
| 30-29      | Reserved                     |
| 28         | RTC_I2C_CLKGate_EN          |
| 6,5        | RTC_I2C_RX_LSB, RTC_I2C_TX_LSB, FIRST |
| 4           | RTC_I2CTransStart            |
| 3           | RTC_I2C_MS_MODE              |
| 2-0         | Reserved                     |

**Description of Bits:**

- **RTC_I2C_SDA FORCE_OUT:** SDA output mode. Options:
  - `0`: open drain
  - `1`: push pull (R/W)
  
- **RTC_I2C_SCL FORCE_OUT:** SCL output mode. Options:
  - `0`: open drain
  - `1`: push pull (R/W)

- **RTC_I2C_MS_MODE:** Set this bit to configure RTC I2C as a master.
  - `(R/W)`
  
- **RTC_I2CTransStart:** Set this bit to 1, RTC I2C starts sending data. 
  - `(R/W)`
  
- **RTC_I2CTransStart:** This bit is used to control the sending mode:
  - `0`: send data from the most significant bit
  - `1`: send data from the least significant bit.
  - `(R/W)`
  
- **RTC_I2CRX_LSB_FIRST:** This bit is used to control the storage mode for received data. Options:
  - `0`: receive data from the most significant bit
  - `1`: receive data from the least significant bit.
  - `(R/W)`
  
- **RTC_I2CCtrl_CLKGate_EN:** RTC I2C controller clock gate.
  - `(R/W)`
  
- **RTC_I2CRESET:** RTC I2C software reset. 
  - `(R/W)`

---

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback