**Title:**
Chapter 21 I2C Controller (I2C)

**Subtitle:**
21.5 Registers

**Body Text:**
The addresses in this section are relative to the I2C base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section [21.4 Register Summary](#).

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Register Description:**
- **Register 21.1. I2C_SCL_LOW_PERIOD_REG (0x0000)**
  - This register is used for configuring the duration of SCL low in master mode, measured by APB clock cycles.
  
- **Register 21.2. I2C_CTR_REG (0x0004)**
  - Various control bits are listed:
    - `I2C_SCL_LOW_PERIOD`: This register is used to configure for how long SCL remains low in master mode, measured by APB clock cycles.
    - `I2C_RX_LSB_FIRST`: Controls the storage mode for received data. (R/W)
      - 1: receive data from the least significant bit;
      - 0: receive data from the most significant bit.
    - `I2C_TX_LSB_FIRST`: Controls sending modes of data to be sent out by I2C. (R/W)
      - 1: send data from the least significant bit;
      - 0: send data from the most significant bit.
    - `I2CTransStart`: Set this bit to start sending the data in tx fifo. (R/W).
    - `I2C_MS_MODE`: Configures module as an I2C Master or Slave by clearing or setting respectively, measured with APB clock cycles.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 
403