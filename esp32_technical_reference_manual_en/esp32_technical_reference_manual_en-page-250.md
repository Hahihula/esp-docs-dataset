**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
Register 12.11. DPORT_PRO_CACHE_CTRL1_REG (0x044)

**Table of Register Bits and Descriptions:**

- **DPORT_PRO_CACHE_MMU_IA_CLR**: Clears PRO cache MMU error flag.
  - Access Type: Read/Write
  - Description: Disables PRO cache MMU.

- **DPORT_PRO_CMMU_PD**: Disables PRO cache MMU (R/W)
  - Access Type: Read/Write

- **DPORT_PRO_CACHE_MASK_OPSDRAM**: Disables access from APP_CPU DRAM1 to PRO cache.
  - Values:
    - `1`: Disable
    - `0`: Enable

- **DPORT_PRO_CACHE_MASK_DROMO**: Disables access from PRO_CPU DROMO to PRO cache (R/W)
  - Access Type: Read/Write
  - Description: Disables access.

- **DPORT_PRO_CACHE_MASK_DRAM1**: Disables access from PRO_CPU DRAM1 to PRO cache.
  - Values:
    - `1`: Disable
    - `0`: Enable

- **DPORT_PRO_CACHE_MASK_IROMO**: Disables access from PRO_CPU IROMO to PRO cache (R/W)
  - Access Type: Read/Write

- **DPORT_PRO_CACHE_MASK_IRAM1**: Disables access from PRO_CPU IRAM1 to PRO cache.
  - Values:
    - `1`: Disable
    - `0`: Enable

- **DPORT_PRO_CACHE_MASK_IRAMO**: Disables access from PRO_CPU IRAMO to PRO cache (R/W)
  - Access Type: Read/Write

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  
Page Number: ESP32 TRM (Version 5.6)