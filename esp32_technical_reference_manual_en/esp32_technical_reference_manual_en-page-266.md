**Chapter Title:**
Chapter 12 DPort Registers

**Section Header:**
Register 12.195. DPORT_APP_CACHE_DBUGO_REG (0x418)

**Table Description and Values:**
- **Columns:** 
  - Bit number range from 30 to 6
  - Binary values for each bit
  
- **Rows:**
  - Each row represents a specific register value with corresponding bits set or reset.

**Text Descriptions under Table:**

1. **DPORT_APP_CACHE_ACCESS_ILLEGAL**: APP CPU’s illegal access CACHÉ address region.
   - Bit descriptions:
     - Bit O: PRO CPU’s illegal access RVAddrRAM (low-high mode) address region
     - Bit 1: APP CPU’s illegal access VAddrRAM address region
     - Bit 2: APP CPU’s illegal access VAddr3 address region
     - Bit 3: APP CPU’s illegal access VAddr2 address region
     - Bit 4: APP CPU’s illegal access VAddr1 address region
     - Bit 5: APP CPU’s illegal access VAddr0 address region

2. **DPORT_APP_CACHE_MMU_ILLEGAL**: APP CPU’s access to invalid CACHÉ entry.
   - (RO) Read-Only
  
3. **Register Description**:
   - Register 12.196. DPORT_IMMU_TABLE[7:0] (n: 0-15) (0x504+4*n)

4. **DPORT_IMMU_TABLE**: Configures Internal SRAM MMU.
   - When n is in range of 0 to 9, reset value is set as O
   - When n ranges from 10 to 15, the values are respectively: R/W

**Footer Information:**
- Page number and document version:
  - "266 ESP32 TRM (Version 5.6)"
  
- Company information at footer left corner:
  - Espressif Systems
  
- Link for feedback submission in blue text on right side of the page.
  - Submit Documentation Feedback