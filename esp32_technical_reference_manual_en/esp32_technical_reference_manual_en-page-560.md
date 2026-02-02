**Title: Chapter 25 Two-Wire Automotive Interface (TWAI)**

---

**Section Title:** Register 25.24. TWAI_TX_ERR_CNT_REG (0x003C)

- **Description:** The TX error counter register, reflects value changes under transmission status.
- **Register Type:** (RO | R/W)
- **Bit Map:**
  - Bit positions are labeled from left to right as follows:
    ```
    31  8   7      0
    ```

**Section Title:** Register 25.25. TWAI_RX_MESSAGE_CNT_REG (0x0074)

- **Description:** This register reflects the number of messages available within the RX FIFO.
- **Register Type:** (RO)
- **Bit Map:**
  - Bit positions are labeled from left to right as follows:
    ```
    31   (reserved)     6      0
    ```

---

**Footer Information:**

- Company Name: Espressif Systems
- Document Version and Reference Number: ESP32 TRM (Version 5.6)
- Page Number: 560

[Submit Documentation Feedback](#)