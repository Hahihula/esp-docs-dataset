**Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table Title:**
Table 4.3-8. MPU for DMA

**Column Headers:**
- Size
- Low Boundary address High Authority Bit 
- Register Internal SRAM 

**Content Summary:** The table lists various memory sizes with corresponding low boundary addresses in hexadecimal format and registers associated with each size.

**Example Entries from the Table (partial):**

1. **Size**: 8 KB  
   **Low Boundary address High Authority Bit**: 0x3FFA_E000, 0x3FFA_FFFF
   **Register Internal SRAM**: DPORT_AHB_MPU_TABLE_0_REG

2. **Size**: 8 KB  
   **Low Boundary address High Authority Bit**: 0x3FFB_0000, 0x3FFB_1FFF
   **Register Internal SRAM**: DPORT_AHB_MPU_TABLE_0_REG

3. **Size**: 8 KB  
   **Low Boundary address High Authority Bit**: 0x3FFB_2000, 0x3FFB_3FFF
   **Register Internal SRAM**: DPORT_AHB_MPU_TABLE_0_REG

4. **Size**: 8 KB  
   **Low Boundary address High Authority Bit**: 0x3FFB_4000, 0x3FFB_5FFF
   **Register Internal SRAM**: DPORT_AHB_MPU_TABLE_0_REG

... (continues with similar entries for other sizes)

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)