**Title:**
Chapter Title (Not fully visible, appears to be related to "Permission Control")

**Register Information:**
- **Register Name:** PMS_CORE_0_DRAMO_PMS_MONITOR_3_REG (0x110)
- **Bit Description Table:**

  - **Field:** 
    - Offset Range: [31, 16]
    - Values:
      - `PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_BYTEEN`
        - Description: Stores the byte information of illegal access. (RO)
      - `PMS_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_STATUS_WR`
        - Description: Stores the direction of unauthorized access. 0: read; 1: write. (RO)

**Bit Values Example:**
- **Example Values:** 
  - Bit positions [31, 16]: `1 0`  
  - Bit position [17, 16]: `0`
  - Bit value at the end of range is labeled as "Reset"

**Footer Information:**
- Document Title (Partially visible): ESP32-S3 TRM (Version 1.7)
- Navigation Link: GoBack

This document appears to be a technical reference manual for an integrated circuit, specifically focusing on memory protection and monitoring registers related to DRAM operations in the context of the ESP32-S3 chip by Espressif Systems.