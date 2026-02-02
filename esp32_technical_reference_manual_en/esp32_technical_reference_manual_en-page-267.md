**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
GoBack

**Register Information (with binary representation):**
- **Register Name:** DPORT_DMMU_TABLEn
- **Address Range:** n = 0-15, Offset: 0x544 + 4*n
- **Description:** Configures Internal SRAM MMU. When `n` is in the range of 0 to 15, reset values are from address offset O to F (0 ~ 15), respectively.
- **Access Mode:** Read/Write

**Register Information:**
- **Register Name:** DPORT_MMU_ACCESS_ILLEGAL_INT_EN_REG
- **Address:** 0x598
- **Description:** 
  - `DPорт_DMA_ACCESS_DENY_INT_EN`: Enables the DMA's access to SRAM denied interrupt.
    - Access Mode: Read/Write (R/W)
  - `DPорт_ACCESS_PID_ILLEGAL_INT_EN`: Enables the CPU’s illegal access to the PID controller interrupt.
    - Bit Description:
      - **Bit 0:** Enables the APP CPU’s illegal access to the PID controller interrupt
      - **Bit 1:** Enables the PRO CPU's illegal access to the PID controller interrupt

**Footer:**
- Page Number: 267
- Company Name and Document Version Information: Espressif Systems, ESP32 TRM (Version 5.6)
- Link Texts:
  - Submit Documentation Feedback