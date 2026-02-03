**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Section Header: Register 34.5. SDHOST_TMR_OUT_REG (0x0014)**

- **Field Name and Value:**
  - `SDHOST_DATA_TIMEOUT`  
    - Description:
      ```
      The value for card data read timeout.
      This value is also used for data starvation by host timeout.

      The timeout counter is started only after the card clock
      is stopped. This value is specified in number of 
      card output clocks, i.e., sdhost_cclk_out of the selected card.

      NOTE: The software timer should be used if the timeout value

      is in order of 100 ms.
      In this case, read data timeout interrupt needs to
      be disabled.
      ```

- **Field Name and Value:**
  - `SDHOST_RESPONSE_TIMEOUT`  
    - Description:
      ```
      Response timeout value.

      The value specified in terms of number of card output clocks,
      i.e., sdhost_cclk_out. (R/W)
      ```

---

**Section Header: Register 34.6. SDHOST_CTYPE_REG (0x0018)**

- **Field Name and Value:**
  - `SDHOST_CARD_WIDTH8`  
    - Description:
      ```
      One bit per card indicates if the card is in
      8-bit mode.

      0: Non 8-bit mode;
      1: 8-bit mode.
      
      Bit[17:16] correspond to card[1:0] respectively.
      ```

- **Field Name and Value:**
  - `SDHOST_CARD_WIDTH4`  
    - Description:
      ```
      One bit per card indicates if the card is in
      1-bit or 4-bit mode.

      0: 1-bit mode;
      1: 4-bit mode.
      
      Bit[1:0] correspond to card[1:0] respectively.
      ```

---

**Footer Information:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

**Page Number and Link for Feedback:** Submit Documentation Feedback

**Diagram Description in Section Header Images:**
- The diagram shows the layout of registers with specific fields labeled, such as `SDHOST_DATA_TIMEOUT` at address `0x0004`, showing a value range from `0x0000` to `0xFFFFF`. 
- Another similar structure is shown for register `SDHOST_CTYPE_REG` starting from address `0x0018`.

**Diagram Description in Section Header Images:**
- The diagram shows the layout of registers with specific fields labeled, such as `SDHOST CARD_WIDTH4` at addresses ranging between 31 to some lower value. 
- Another similar structure is shown for register `SDHOST CARD_WIDTH8`.