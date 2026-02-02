**Title:**
Chapter 3 System and Memory

**Diagram Title:**
Figure 3.2-2. System Address Mapping

**Diagram Labels (from left to right, top to bottom):**

1. **External Flash**: 
   - Arrow pointing towards MMU with label "24"

2. **MMU**:
   - Connected by arrows from Cache and External SRAM
   - Connected via lines labeled 0x3F7F_FFFF

3. **Cache**
   - Connected to MMU, ROM, and DMA (Direct Memory Access)

4. **ROM**: 
   - Labeled with addresses: 0x3FF8_2000; 0x3FF9_FFFF
   - Connected via lines labeled from Cache at address "23"

5. **Peripheral**
   - Listed memory ranges:
     - 0x0000_0000 to 0x3F7F_FFFF

6. **DMA** (Direct Memory Access):
   - Labeled with addresses: 0x4008_0000; 0x400B_FFFF
   - Connected via lines labeled from Cache at address "23"

7. **FAST Memory**
   - Listed memory ranges:
     - 0x400C_0000 to 0x5000_1FFF

8. **SLOW Memory** (RTC)
   - Labeled with addresses: 
     - 0x5000_2000; 0xFFFF_FFFF
   - Connected via lines labeled from Cache at address "23"

9. **External SRAM**: 
   - Arrow pointing towards MMU

10. **RTC**
    - Listed memory ranges:
      - 0x408F_FFFF to 0x5000_1FFF
    - Connected via lines labeled from Cache at address "23"

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)