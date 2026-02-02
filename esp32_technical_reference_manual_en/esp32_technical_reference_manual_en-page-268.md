**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
Register 12.199, DPORT MPU_ACCESS_ILLEGAL_INT_EN REG (0x59C)

**Diagram Description:**
A diagram showing the layout of a register with labeled fields:
- DPORT_MEM_MMU_MULTI_HIT_IN
- DPORT_MEM_ACCESS_DENY_INT_EN
- Reserved bits

**Field Descriptions and Values in Binary:**

1. **DPORT_MEM_MMU MULTI HIT INT EN (31-0)**
   - 31, 24, 23, ..., 8, 7, 4, 3, 0
  
2. **Reset Value:** 
   - All bits are set to '0'.

**Field Descriptions:**

- **DPORT_MEM_MMU MULTI HIT INT EN**
  - Enables the SRAM MMU configuration error interrupt.
    - Bit 0: Enables multiple entry hit interrupt when APP CPU accesses SRAMO
    - Bit 1: Enables multiple entry hit interrupt when PRO CPU accesses SRAMO
    - Bit 2: Enables multiple entry hit interrupt when APP CPU accesses SRAM2
    - Bit 3: Enables multiple entry hit interrupt when PRO CPU accesses SRAM2 (R/W)

- **DPORT_MEM_ACCESS_ILLEGAL_INT_EN**
  - Enables CPU address overflow interrupt when accessing SRAM.
    - Bit O-1: reserved
    - Bit 2: Enables address overflow interrupt when APP CPU accesses SRAMO
    - Bit 3: Enables address overflow interrupt when PRO CPU accesses SRAMO
    - Bits 4 to 7: reserved

- **DPORT_MEM_ACCESS_DENY_INT_EN**
  - Enables the CPU’s access to SRAM denied interrupt.
    - Bit 0: Enables denied interrupt when APP CPU accesses SRAMO
    - Bit 1: Enables denied interrupt when PRO CPU accesses SRAMO
    - Bit 2: Enables denied interrupt when APP CPU accesses SRAM2
    - Bit 3: Enable denied interrupt when PRO CPU accesses SRAM2 (R/W)

**Footer Information:**
Espressif Systems  
Page number: 268  
Document version: ESP32 TRM (Version 5.6)  
Link to submit documentation feedback