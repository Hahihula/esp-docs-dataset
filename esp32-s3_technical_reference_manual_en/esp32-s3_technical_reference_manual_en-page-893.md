**Title: Chapter 21 HMAC Accelerator (HMAC)**

**GoBack**

---

### Register 21.4. HMAC_SET_PARA_FINISH_REG (0x04C)

- **Field:** HMAC_SET_PARA_END  
  - Description: Set this bit to finish HMAC configuration.
  - Access Mode: WO
  - Bit Mask Diagram:
    ```
    31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    (reserved) Reset HMAC_SET_PARA_END
    ```

---

### Register 21.5. HMAC_SET_MESSAGE_ONE_REG (0x050)

- **Field:** HMAC_SET_TEXT_ONE  
  - Description: Call SHA to calculate one message block.
  - Access Mode: WO
  - Bit Mask Diagram:
    ```
    31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    (reserved) Reset HMAC_SET_TEXT_ONE
    ```

---

### Register 21.6. HMAC_SET_MESSAGE_ING_REG (0x054)

- **Field:** HMAC_SET_TEXT_ING  
  - Description: Set this bit to show there are still some message blocks to be processed.
  - Access Mode: WO
  - Bit Mask Diagram:
    ```
    31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
    (reserved) Reset HMAC_SET_TEXT_ING
    ```

---

**Footer:**
- Espressif Systems, ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback