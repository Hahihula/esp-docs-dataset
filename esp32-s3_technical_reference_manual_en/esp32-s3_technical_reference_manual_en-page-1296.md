**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Link:**
GoBack

**Register Information:**
- Register Name: SDHOST_STATUS_REG (0x0048)
- Description:
  - Continued from the previous page ...

**Status Definitions:**

1. **SDHOST_FIFO_FULL**: FIFO is full status.
   - Access Type: Read Only
2. **SDHOST_FIFO_EMPTY**: FIFO is empty status.
   - Access Type: Read Only

3. **SDHOST_FIFO_TX_WATERMARK**: FIFO reached Transmit watermark level, not qualified with data transfer.
   - Access Type: Read Only (RO)
4. **SDHOST_FIFO_RX_WATERMARK**: FIFO reached Receive watermark level, not qualified with data transfer.
   - Access Type: Read Only
   - Note: This is repeated twice in the document.

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Reference Number:
  - Page number: 1296
  - Document Title: ESP32-S3 TRM (Version 1.7)
- Link for Submitting Documentation Feedback