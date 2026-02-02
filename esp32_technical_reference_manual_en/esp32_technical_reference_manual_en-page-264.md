**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
Register 12.192. DPORT_MEM_ACCESS_DBUGO_REG (0x3E8)

**Table Description with Labels and Values:**
- **DPORT_MEM_MMU MULTI HIT**: Indicates configuration errors of SRAM MMU.
  - Bit 0: APP CPU hits multiple entries when accessing SRAMO
  - Bit 1: PRO CPU hits multiple entries when accessing SRAMO
  - Bit 2: APP CPU hits multiple entries when accessing SRAM2
  - Bit 3: PRO CPU hits multiple entries when accessing SRAM2 (RO)

- **DPORT_MEM_ACCESS_ILLLEGAL**: CPU address overflow when accessing SRAM.
  - Bit 0-1: reserved
  - Bit 2: APP CPU address overflow when accessing SRAMO
  - Bit 3: PRO CPU address overflow when accessing SRAMO
  - Bit 4-7: reserved
  - Bit 8: APP CPU address overflow when accessing SRAM2
  - Bit 9: PRO CPU address overflow when accessing SRAM3.
  - Bit 10-11: reserved (RO)

- **DPORT_MEM_ACCESS_DENY**: CPU’s access to SRAM is denied.
  - Bit 0: APP CPU's access to SRAMO is denied
  - Bit 1: PRO CPU's access to SRAMO is denied
  - Bit 2: APP CPU's access to SRAM2 is denied
  - Bit 3: PRO CPU’s access to SRAM2 (RO) is denied

**Footer Information:**
Espressif Systems  
Page Number: 264  
Document Version: ESP32 TRM (Version 5.6)

**Navigation Link:**
GoBack