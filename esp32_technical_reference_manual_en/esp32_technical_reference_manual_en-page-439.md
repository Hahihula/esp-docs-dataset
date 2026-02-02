**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Register Information:**

- **Register Name:** Register 22.9. I2S_FIFO_CONFIG_REG (0x0020)
  - **Hexadecimal Breakdown of the Register:**
    ```
    31       21      20      19      18      16      15      14      13      12      11      10      9       8       7       6       5       4       3       2       1       0
    I2S_RX_FIFO_MOD FORCE_EN   The bit should always be set to 1. (R/W)
    I2S_TX_FIFO_MOD FORCE_EN   The bit should always be set to 1. (R/W)
    I2S_RX_FIFO_MOD            Receive FIFO mode configuration bit. (R/W)
    I2S_TX_FIFO_MOD            Transmit FIFO mode configuration bit. (R/W)
    I2S_DSCR_EN                Set this bit to enable I2S DMA mode. (R/W)
    I2S_TX_DATA_NUM            Threshold of data length in the transmit FIFO. (R/W)
    I2S_RX_DATA_NUM            Threshold of data length in the receive FIFO. (R/W)
    ```

- **Register Name:** Register 22.10. I2S_RXEOF_NUM_REG (0x0024)
  - Description: The length of the data to be received.
  - Functionality Note:
    ```
    This will trigger I2S_IN_SUC_EOF_INT.
    ```

- **Register Name:** Register 22.11. I2S_CONF_SINGLE_DATA_REG (0x0028)
  - Description: The right channel or the left channel outputs constant values stored in this register according to TX_CHAN_MOD and I2S_TX_MSB_RIGHT.

**Footer Information:**
- Page Number: 439
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Navigation Links:** 
- Submit Documentation Feedback