**Title:**
Chapter 12 DPort Registers

**Back to Top Link:** GoBack

**Subheading and Register Information (with binary representation):**
Register 12.12. DPOR_APP_CACHE_CTRL_REG (0x58)

| Field Name | Binary Representation |
|------------|-----------------------|
| Reserved   | 00000000             |
| DPORT_APP_DRAM_HL | 00000000          |
| DPORT_APPDRAM_SPLIT | 00000000         |
| DPORT_APP_SINGLE_IRAM_ENA | 00000000       |
| Reserved   | 00000000           |
| DPOR_APP_CACHE_FLUSH_DONE | 00000000    |
| DPOR_APP_CACHE_FLUSH_ENA | 00000000     |
| DPOR_APP_CACHE_ENABLE | 00000000      |

**Field Descriptions:**
- **DPOR_APP_DRAM_HL:** Determines the virtual address mode of the External SRAM. (R/W)
- **DPOR_APPDRAM_SPLIT:** Determines the virtual address mode of the External SRAM. (R/W)
- **DPOR_APP_SINGLE_IRAM_ENA:** Determines a special mode for APP_CPU access to the external flash. (R/W)
- **DPOR_APP_CACHE_FLUSH_DONE:** APP_CPU cache-flush done. (RO)
- **DPOR_APP_CACHE_FLUSH_ENA:** Flushes the APP_CPU cache. (R/W)
- **DPOR_APP_CACHE_ENABLE:** Enables the APP_CPU cache. (R/W)

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**
ESP32 TRM (Version 5.6)