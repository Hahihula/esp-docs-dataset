**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
GoBack

**Register Information (with binary representation):**

- **Register Name:** DPORT_MEM_ACCESS_DBUG1_REG (0x3EC)
  - Description:
    - DPRT_DMA_ACCESS_DENY DMA’s access to SRAM is denied. (RO)
    - DPRT_ACCESS_PID_ILLEGAL CPU’s access to the PID controller is illegal.
      - Bit O: APP CPU’s illegal access to the PID controller
      - Bit I: PRO CPU’s illegal access to the PID controller

- **Register Name:** DPORT_MEM_ACCESS_MISS CPU’s access to SRAM is denied.
  - Description:
    - Bit O: APP CPU’s access to SRAMO is denied
    - Bit B: PRO CPU’s access to SRAM0 is denied

- **Register Name:** DPRT_PRO_CACHE_DBUG0_REG (0x3F0)
  - Description:
    - DPRT_PRO_CACHE_ACCESS_ILLEGAL PRO CPU’s illegal access to CACHE address region.
      - Bit O: APP CPU’s illegal access to VAddrRAM (low-high mode) address region
      - Bit I: PRO CPU’s illegal access to VAddrRAM address region

- **Register Name:** DPRT_PRO_CACHE_MMU_ILLEGAL PRO CPU’s access to invalid CACHE entry. (RO)
  - Description:
    - Bit B: PRO CPU’s illegal access to VAddr2 address region
    - Bit I: PRO CPU’s illegal access to VAddr1 address region

**Footer Information:**
Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback