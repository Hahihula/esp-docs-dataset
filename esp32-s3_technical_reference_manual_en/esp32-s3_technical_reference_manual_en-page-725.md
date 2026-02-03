**Title:**
Chapter 15: Permission Control (PMS)

**Register Information:**
- **Register Name:** PMS_DMA_APBPERI_AES_PMS CONSTRAINT O_REG (0x0070)
- **Field Description:** 
  - **Name:** PMS_DMA_APBPERI_AES_PMS CONSTRAINT LOCK
  - **Function:** Set this bit to lock AES's GDMA permission configuration register. (R/W)

**Bit Layout:**
```
+-------------+
|   31       |    0 |
|  30-24     |    0 |
|  23-16     |    0 |
|  15-8      |    0 |
|  7-0      |    0 |
+-------------+
```
- **Field Values:**
  - Bit positions are labeled from right to left.
  - The bit at position `31` is highlighted with a label indicating it can be reset.

**Footer Information:**
- Document version and feedback information:
  - "Submit Documentation Feedback"
  - Page number (725)
  - Document title or identifier ("ESP32-S3 TRM (Version 1.7)")

This document appears to describe the configuration register for AES's GDMA permission control in a specific context, likely related to hardware programming instructions and specifications provided by Espressif Systems.