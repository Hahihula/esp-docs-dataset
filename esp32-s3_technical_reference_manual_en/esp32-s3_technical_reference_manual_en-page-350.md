**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**Section Title: Register 2.26. RTC_I2C_INT_ENA_REG (0x0030)**

- **Diagram Description:** 
  - A bit map showing the register layout with labels for each interrupt enable bits.

- **Text Content in Diagram Labels:**
  - `RTC_I2C_SLAVE_TRAN_COMP_INT_ENA`
  - `RTC_I2C_SLAVE_TRAN_COMP_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_ARBITRATION_LOST_INT_ENA`
  - `RTC_I2C_ARBITRATION_LOST_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_MASTER_TRAN_COMP_INT_ENA`
  - `RTC_I2C_MASTER_TRAN_COMP_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_TRANSComplete_INT_ENA`
  - `RTC_I2C_TRANSComplete_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_TIMEOUT_INT_ENA`
  - `RTC_I2C_TIMEOUT_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_ACK_ERR_INT_ENA`
  - `RTC_I2C_ACK_ERR_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_RX_DATA_INT_ENA`
  - `RTC_I2C_RX_DATA_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_TX_DATA_INT_ENA`
  - `RTC_I2C_TX_DATA_INT` (interrupt enable bit. R/W)
  - `RTC_I2C_DETECT_START_INT_ENA`
  - `RTC_I2C_DETECT_START_INT` (interrupt enable bit. R/W)

**Section Title: Register 2.27. RTC_I2C_DATA_REG (0x0034)**

- **Diagram Description:** 
  - Another bit map showing the register layout with labels for each data received or sent.

- **Text Content in Diagram Labels:**
  - `RTC_I2C_RDATA` Data received. (RO)
  - `RTC_I2C_SLAVE_TX_DATA` The data sent by slave. (R/W)
  - `RTC_I2C_DONE` RTC I2C transmission is done. (RO)

**Footer Information:** 
- "Espressif Systems"
- Page number: **350**
- Document version and type information:
  - ESP32-S3 TRM (Version 1.7)