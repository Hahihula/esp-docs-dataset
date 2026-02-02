**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table Titles with Descriptions:**

1. **Table 4.3-15. Virtual Address for External SRAM (Normal Mode)**
   - Columns:
     - "Virtual address"
     - "Size" 
     - "Low PRO_CPU address"
     - "High PRO_CPU address"
   - Rows:
     - "LVAaddrRAM", Size: 4 MB, Low: 0x3F80_0000, High: 0x3FBF_FFFF
     - "Virtual address" (repeated), Size and addresses are the same as above

2. **Table 4.3-16. Virtual Address for External SRAM (Low-High Mode)**
   - Columns:
     - "Virtual address"
     - "Size"
     - "PRO_CPU/APP_CPU address Low"
     - "High PRO_CPU/APP_CPU address"
   - Rows:
     - "LVAaddrRAM", Size: 2 MB, Low: 0x3F80_0000, High: 0x3FBF_FFFF
     - "RVAaddrRAM" (repeated), addresses are the same

3. **Table 4.3-17. Virtual Address for External SRAM (Even-Odd Mode)**
   - Columns:
     - "Virtual address"
     - "Size"
     - "Low PRO_CPU/APP_CPU address"
     - "High PRO_CPU/APP_CPU address"
   - Rows with repeated entries: 
     - "LVAaddrRAM", Size and addresses are 32 Bytes, Low: 0x3F80_0000 to High: 0x3FBF_FFDF
     - "RVAaddrRAM" (repeated), sizes remain the same

**Text Explanation in Between Tables:**
- In **Low-High mode**, both the PRO_CPU and APP_CPU use the same mapping entries. The lower part of virtual address space is used for LVAaddrRAM, while RVAaddrRAM uses upper 2 MB.
- In Even-Odd memory configuration:
  - VRAM split into chunks (32-byte).
  - MMU resolves even chunks through specific addresses; odd chunks map to the same values as even ones.

**Additional Information:**
- The bit configuration of External RAM MMU entries is similar for flash memory, with details on physical page mapping and valid bits.
- Table reference:
  - "Table 4.3-18" describes first MMU entry number (LVAaddrRAM) across all PIDs in detail.

**Footer:**
- Page Number: 87
- Document Version: ESP32 TRM (Version 5.6)
- Company Name and Submission Information:
  - Espressif Systems, Submit Documentation Feedback