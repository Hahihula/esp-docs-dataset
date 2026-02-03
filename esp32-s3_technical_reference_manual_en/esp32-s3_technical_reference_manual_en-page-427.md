**Title:**
Chapter 5 eFuse Controller

**Section Title:**
5.5 Registers

**Body Text:**
The addresses in this section are relative to eFuse Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection with Diagrams (Descriptive Captions):**

1. **Register 5.1:** EFUSE_PGM_DATA0_REG (0x0000)
   - Diagram: Shows a register labeled "EFUSE_PGM_DATA0" at address `0x000000` and another label indicating the bit position as '31' with an arrow pointing to it.
   
2. **Register 5.2:** EFUSE_PGM_DATA1_REG (0x0004)
   - Diagram: Similar layout showing "EFUSE_PGM_DATA1" at address `0x000000` and the bit position '31' indicated.

3. **Register 5.3:** EFUSE_PGM_DATA2_REG (0x0008)
   - Diagram: Shows a register labeled "EFUSE_PGM_DATA2" with an arrow pointing to address `0x000000` and the bit position '31'.

**Descriptions of Registers in Text Format:**

- **Register 5.1:** EFUSE_PGM_DATA0
  - Configures the content of the Oth 32-bit data to be programmed.
  
- **Register 5.2:** EFUSE_PGM_DATA1
  - Configures the content of the 1st data to be programmed.

- **Register 5.3:** EFUSE_PGM_DATA2
  - Configures the content of the 2nd 32-bit data to be programmed.
  
**Footer:**
Espressif Systems

Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)