**Title:**
Chapter 28 I2S Controller (I2S)

**Subtitles and Sections:**

1. **Register 28.3. I2S_INT_ENA_REG (0x0014)**
   - Description:
     ```
     0  O  O  O  O  O  O  O  O  O  O  O  O  O  O  O  Reset
     ```
   - Details of bits and their functions in hexadecimal format with descriptions below each bit.
     - `I2S_RXDone_INT_ENA`: The interrupt enable bit for I2S_RX_DONE_INT interrupt. (R/W)
     - `I2S_TXDone_INT_ENA`: The interrupt enable bit for I2S_TX_DONE_INT interrupt. (R/W)
     - `I2S_RxHung_INT_ENA`: The interrupt enable bit for I2S_RX_HUNG_INT interrupt. (R/W)
     - `I2S_TxHung_INT_ENA`: The interrupt enable bit for I2S_TX_HUNG_INT interrupt. (R/W)

2. **Register 28.4. I2S_INT_CLR_REG (0x0018)**
   - Description:
     ```
     0  O  O  O  O  O  O  O  O  O  O  O  Reset
     ```
   - Details of bits and their functions in hexadecimal format with descriptions below each bit.
     - `I2S_RXDone_INT_CLR`: Set this bit to clear I2S_RX_DONE_INT interrupt. (WT)
     - `I2S_TXDone_INT_CLR`: Set this bit to clear I2S_TX_DONE_INT interrupt. (WT)
     - `I2S_RxHung_INT_CLR`: Set this bit to clear I2S_RX_HUNG_INT interrupt. (WT)
     - `I2S_TxHung_INT_CLR`: Set this bit to clear I2S_TX_HUNG_INT interrupt. (WT)

**Footer:**
- Page number and document version information:
  ```
  Espressif Systems
  ESP32-S3 TRM (Version 1.7)
  Submit Documentation Feedback