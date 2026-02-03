**Title: Chapter 34 SD/MMC Host Controller (SDHOST)**

**Subtitle: Register 34.33. SDHOST_IDSTS_REG (0x008C)**
- **GoBack**

**Table Description:**  
The table shows the layout of register `SDHOST_IDSTS_REG` with various fields and their bit positions.

**Field Descriptions in Markdown Format:**

1. **SDHOST_IDSTS_FSM**
   - **Description**: DMA FSM present state (RO)
     - 0: DMA_IDLE (idle state);
     - 1: DMA_SUSPEND (suspend state);
     - 2: DESC_RD (descriptor reading state);
     - 3: DESC_CHK (descriptor checking state);
     - 4: DMA_RD_REQ_WAIT (read-data request waiting state);
     - 5: DMA_WR_REQ_WAIT (write-data request waiting state);
     - 6: DMA_RD (data-read state);
     - 7: DMA_WR (data-write state);
     - 8: DESC_CLOSE (descriptor close state).

2. **SDHOST_IDSTS_FBE_CODE**
   - **Description**: Fatal Bus Error Code
     - Indicates the type of error that caused a Bus interrupt.
     - Valid only when the Fatal Bus Error bit IDSTS[2] is set.

3. **SDHOST_IDSTS_AIS**
   - **Description**: Abnormal Interrupt Summary (Logical OR)
     - 0: DMA bit Interrupt; Unmasked bits affect this bit, sticky and must be cleared each time a corresponding bit that causes AIS to be set.
     - Writing `1` clears the bit.

4. **SDHOST_IDSTS_NIS**
   - **Description**: Normal Interrupt Summary (Logical OR)
     - 0: Transmit Interrupt
     - Unmasked bits affect this bit, sticky and must be cleared each time a corresponding bit that causes NIS to be set.
     - Writing `1` clears the bit.

**Footer:**  
Continued on the next page...

**Document Information at Bottom of Page:**  
- **Company**: Espressif Systems
- **Page Number**: 1304
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Links**: Submit Documentation Feedback