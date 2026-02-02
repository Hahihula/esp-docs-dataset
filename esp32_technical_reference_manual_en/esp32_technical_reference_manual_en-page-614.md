**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

### Register Section:

#### **Register 27.5. TMOUT_REG (0x0014)**

- **DATA_TIMEOUT**: 
  - Description:
    - Value for card data read timeout.
    - This value is also used for data starvation by host timeout.
    - The timeout counter is started only after the card clock is stopped.
    - This value is specified in number of card output clocks, i.e., `cclk_out` of the selected card.

  - Note:
    - The software timer should be used if the timeout value is in the order of 100 ms. In this case, read data timeout interrupt needs to be disabled.
    - (R/W)

- **RESPONSE_TIMEOUT**:
  - Description: 
    - Response timeout value.
    - Value is specified in terms of number of card output clocks, i.e., `cclk_out`.
    - (R/W)

---

#### **Register 27.6. CTYPE_REG (0x0018)**

- **CARD_WIDTH8**:
  - Description: 
    - One bit per card indicates if the card is in 8-bit mode.
    - Options:
      - `0`: Non 8-bit mode;
      - `1`: 8-bit mode.

  - Note:
    - Bit[16:17] correspond to card[1:0] respectively. (R/W)

- **CARD_WIDTH4**:
  - Description: 
    - One bit per card indicates if the card is in 1-bit or 4-bit mode.
    - Options:
      - `0`: 1-bit mode;
      - `1`: 4-bit mode.

  - Note:
    - Bit[1:0] correspond to card[1:0] respectively. Only `NUM_CARDS*2` number of bits are implemented. (R/W)

---

#### **Register 27.7. BLKSIZ_REG (0x001C)**

- **BLOCK_SIZE**:
  - Description: 
    - Block size.
    - Options represented in binary format.

---

**Footer Information:**  
Espressif Systems  
614 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback