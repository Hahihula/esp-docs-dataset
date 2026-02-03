**Chapter Title:**
Chapter 15 Permission Control (PMS)

**Table Reference and Content:**
- **Title:** Table 15.3-14. RTC SLOW Memory Address

| RTC SLOW Memory | Starting Address | Ending Address |
|------------------|------------------|---------------|
| RTCSlow_0        | 0x5000_0000      | 0x5000_1FF    |
| RTCSlow_1        | 0x6002_1000      | 0x6002_2FFF   |

**Subsection Title:**
15.3.4.2 Access Configuration

**Body Text:**
Both ESP32-S3’s RTCSlow_0 and RTCSlow_1 can be further split into two regions. Each split region can be configured independently with different access by configuring respective registers (PMS_CORE_m_PIF_PMS_CONSTRAN_n_REG).

Note that split regions can be configured independently for CPU0 and CPU1 and for the Secure World and Non-secure World.

The registers for splitting RTC SLOW Memory into 4 split regions are described below:

**Table Title:**
Table 15.3-15. Split RTCSlow_0 and RTCSlow_1 into Split Regions

| Memory | Split Regions | Configuration Registers |
|--------|---------------|-------------------------|
|        | Secure World  | Non-Secure World       |
| Higher Region | RTCSlow_0    | PIF_PMS_CONSTRAN_11_REG [10:0] | PIF_PMS_CONSTRAN_9_REG [21:11] |
| Lower Region   |               |                        |                                |
| Higher Region  | RTCSlow_1   | PIF_PMS_CONSTRAN_13_REG [10:0] | PIF_PMS_CONSTRAN_13_REG [21:11] |

**Footnote:**
The offset from the RTC SLOW Memory base address should be used when configuring the split address. For example, if you want to split the RTC SLOW Memory at 0x6002_2000, then write 0x1000 to this register.

Access configuration to the split regions of RTC SLOW Memory is described below:

**Table Title:**
Table 15.3-16. Access Configuration to the RTC SLOW Memory

| Bus | Mem   | Split Regions | Non-Secure World |
|-----|-------|---------------|------------------|
|     | Higher A | PIF_PMS_CONSTRAN_12_REG [5:3] C | PIF_PMS_CONSTRAN_12_REG [11:9] |
| Peri Slow_0  | Lower B   | PIF_PMS_CONSTRAN_12_REG [8:6]    | PIF_PMS_CONSTRAN_12_REG [8:6]   |
| Bus (PIF) RTC Slow_1 | Higher A | PIF_PMS_CONSTRAN_14_REG [5:3] C  | PIF_PMS_CONSTRAN_14_REG [11:9]  |
|                  | Lower B   | PIF_PMS_CONSTRAN_14_REG [2:0]    | PIF_PMS_CONSTRAN_14_REG [8:6]   |

**Footnotes in Table:**
- A Higher is short for Higher Region.
- B Lower is short for Lower Region.

C For example, configuring this field to 0b100 indicates CPU’s peripheral (PIF) bus is granted with the instruction execution access but not the write or read accesses from the Secure WORLD to the higher region of RTCSLOW_0.

**Subsection Title:**
15.4 Peripherals

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
693 Submit Documentation Feedback