**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Section Titles and Descriptions with Details from Image Content:**

- **Register 21.5, I2C_SLALE_ADDR_REG (0x001D)**
  - **Field Description:** 
    - `I2C_SLAVE_ADDR_10BIT_EN`  
      This field is used to enable the slave 10-bit addressing mode in master mode.
      - **Access Mode:** Read/Write
    - `I2C_SLALE_ADDR`
      When configured as an I2C Slave, this field is used to configure the slave address. 
      - **Access Mode:** Read/Write

- **Register 21.6, I2C_RXFIFO_ST_REG (0x001D)**
  - **Field Description:**
    - `I2C_TXFIFO_END_ADDR`
      This is the offset address of the last sent data, as described in nonfiffo_tx_thres register.
      The value refreshes when I2C_TX_SEND_EMPTY_INT or I2CTransComplete_INT interrupt is generated. 
      - **Access Mode:** Read/Write
    - `I2C_TXFIFO_START_ADDR`
      This is the offset address of the first sent data, as described in nonfifo_tx_thres register.
      - **Access Mode:** Read/Only
    - `I2C_RXFIFO_END_ADDR`
      This is the offset address of the last received data, as described in nonfiffo_rx_thres register. 
      The value refreshes when I2C_RX_REC_FULL_INT or I2CTransComplete_INT interrupt is generated.
      - **Access Mode:** Read/Only
    - `I2C_RXFIFO_START_ADDR`
      This is the offset address of the last received data, as described in nonfifo_rx_thres register. 
      - **Access Mode:** Read/Only

**Footer:**
- Espressif Systems
- Page Number and Document Version Information:
  - "405 ESP32 TRM (Version 5.6)"
- Links for Submitting Documentation Feedback