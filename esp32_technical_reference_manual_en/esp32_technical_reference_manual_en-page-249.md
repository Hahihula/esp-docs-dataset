**Title:**
Chapter 12 DPort Registers

**Back Link:**
GoBack

**Subheading and Register Information (with binary representation):**
Register 12.10, DPORT_PRO_CACHE_CTRL_REG (0x040)

| Field | Offset |
|-------|--------|
| DPORT_PRO_DRAM_SPLT | reserved |
| DPORT_PRO_CACHE_FLUSH_DONE | reserved |
| DPORT_PRO_CACHE_FLUSH_ENA | reserved |
| DPORT_PRO_CACHE_ENABLE | 31-28 |

**Body Text:**
DPRT_PRODRAM_HL Determines the virtual address mode of the external SRAM. (R/W)

DPRT_PRODRAM_SPLIT Determines the virtual address mode of the external SRAM. (R/W)

DPRT_PRO_SINGLE_IRAM_ENA Determines a special mode for PRO_CPU access to the external flash. (R/W)

DPRT_PRO_CACHE_FLUSH_DONE PRO_CPU cache-flush done. (RO)

DPRT_PRO_CACHE_FLUSH_ENA Flushes the PRO_CPU cache. (R/W)

DPRT_PRO_CACHE_ENABLE Enables the PRO_CPU cache. (R/W)

**Footer:**
Espressif Systems
249 ESP32 TRM (Version 5.6)
Submit Documentation Feedback