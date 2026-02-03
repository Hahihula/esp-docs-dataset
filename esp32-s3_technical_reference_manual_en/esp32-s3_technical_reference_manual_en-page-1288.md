**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

**Register Section Header and Description:**

1. **Register Name**: Register 34.7. SDHOST_BLKSIZE_REG (0x001C)
   - **Description**: 
     - `SDHOST_BLOCK_SIZE` Block size.
     - `(R/W)` Read/Write
   - **Hexadecimal Values**:
     - 31: [Blank]
     - 16-15: Blank space with a value of "0"
     - X: Blank

2. **Register Name**: Register 34.8. SDHOST_BYTCNT_REG (0x0020)
   - **Description**:
     - `SDHOST_BYTCNT` Number of bytes to be transferred, should be an integral multiple of Block size for block transfers.
     - For data transfers of undefined byte lengths, byte count should be set to 0. When byte count is set to 0, it is the responsibility of host to explicitly send stop/abort command to terminate data transfer.
   - **Hexadecimal Values**:
     - 31: [Blank]
     - X: Blank

**Footer Information:**
- Page Number and Document Version
  - "1288 ESP32-S3 TRM (Version 1.7)"
  
**Company Name**: Espressif Systems
  
**Link for Submitting Documentation Feedback**: 
- Text link labeled as `Submit Documentation Feedback`