**Chapter Title:**
Chapter 21 I2C Controller (I2C) Register

**Register Name and Address:**
21.7. I2C_FIFO_CONF_REG (0x0018)

**Table Description with Labels for Each Bit Field in the Register:**
- `31` to `0`: Various labels such as "reserved", "I2C_NONFIFO_TX_THRES", etc.
- The table shows bit positions and their corresponding register fields.

**Text Descriptions of Register Fields (with explanations):**

- **I2C_NONFIFO_TX_THRES**
  - When I2C sends more than nonfifo_tx_thres bytes of data, it will generate a `tx_send_empty_int_raw` interrupt and update the current offset address of the sent data. (R/W)

- **I2C_NONFIFO_RX_THRES**
  - When I2C receives more than nonfifo_rx_thres bytes of data, it will generate a `rx_send_full_int_raw` interrupt and update the current offset address of the received data. (R/W)

- **I2C_FIFO_ADDR_CFG_EN**
  - This bit is set to enable APB nonfifo access when this byte after I2C address represents the offset address in the I2C Slave RAM.

- **I2C_NONFIFO_EN**
  - Set this bit to enable APB nonfifo access. (R/W)

- **I2C_TXFIFO_EMPTY_THRHD**
  - Configures the TX FIFO threshold in non-FIFO mode.
  - When the TX FIFO count is greater than I2C_TXFIFO_EMPTYThrhd[4:0], `I2C_TXFIFO_EMPTY_INT_RAW` bit is valid. (R/W)

- **I2C_RXFIFO_FULL_THRHD**
  - Configures the RX FIFO threshold in non-FIFO mode.
  - When the RX FIFO count is greater than I2C_RXFIFO_FULLThrhd[4:0], `I2C_RXFIFO_FULL_INT_RAW` bit is valid. (R/W)

**Footer Information:**
- Page number and document version information:
  - "Espressif Systems"
  - "ESP32 TRM (Version 5.6)"
  - "Submit Documentation Feedback"