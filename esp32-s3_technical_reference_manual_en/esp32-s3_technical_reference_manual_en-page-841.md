**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**GoBack Link:** GoBack

**Section Header:**
Register 17.23. SYSCON_MEM_POWER_DOWN_REG (0x00AC)

**Binary Representation Diagram and Description of Register:**
- Binary representation diagram showing the bits from most significant bit to least.
- Description:
  - `SYSCON_ROM_POWER_DOWN`: Set this field to send the internal ROM into retention state. (R/W)
  - `SYSCON_SRAM_POWER_DOWN`: Set this field to send the internal SRAM into retention state. (R/W)

**Section Header:**
Register 17.24. SYSCON_MEM_POWER_UP_REG (0x00B0)

**Binary Representation Diagram and Description of Register:**
- Binary representation diagram showing the bits from most significant bit to least.
- Description:
  - `SYSCON_ROM_POWER_UP`: Set this field to force the internal ROM to work as normal (do not enter the retention state) when the chip enters light sleep. (R/W)
  - `SYSCON_SRAM_POWER_UP`: Set this field to force the internal SRAM to work as normal (do not enter the retention state) when the chip enters light sleep. (R/W)

**Footer:**
Espressif Systems
841 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback