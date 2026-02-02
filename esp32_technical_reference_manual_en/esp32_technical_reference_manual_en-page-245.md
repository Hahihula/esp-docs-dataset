**Chapter Title:**
Chapter 12 DPort Registers

**Table of DPort Registers**

| Name                                      | Description                                                                                   | Address            | Access |
|-------------------------------------------|----------------------------------------------------------------------------------------------|--------------------|--------|
| DPOR_DMMU_TABLE11_REG                    | MMU register 1 for internal SRAM 2                                                          | 0x3FF00570         | R/W    |
| DPOR_DMMU_TABLE12_REG                    | MMU register 1 for internal SRAM 2                                                          | 0x3FF00574         | R/W    |
| DPOR_DMMU_TABLE13_REG                    | MMU register 1 for internal SRAM 2                                                          | 0x3FF00578         | R/W    |
| DPOR_DMMU_TABLE14_REG                    | MMU register 1 for internal SRAM 2                                                          | 0x3FF0057C         | R/W    |
| DPOR_DMMU_TABLE15_REG                    | MMU register 1 for internal SRAM 2                                                          | 0x3FF00580         | R/W    |

**APP_CPU Controller Registers**

| Name                                      | Description                                                                                   | Address            | Access |
|-------------------------------------------|----------------------------------------------------------------------------------------------|--------------------|--------|
| DPOR_APPCPU_CTRL_REG_A_REG               | reset for APP_CPU                                                                            | 0x3FF0002C         | R/W    |
| DPOR_APPCPU_CTRL_REG_B_REG               | clock gate for APP_CPU                                                                       | 0x3FF00030         | R/W    |
| DPOR_APPCPU_CTRL_REG_C_REG               | stall for APP_CPU                                                                            | 0x3FF00034         | R/W    |
| DPOR_APPCPU_CTRL_REG_D_REG               | boot address for APP_CPU                                                                      | 0x3FF00038         | R/W    |

**Peripheral Clock Gating and Reset Registers**

| Name                                      | Description                                                                                   | Address            | Access |
|-------------------------------------------|----------------------------------------------------------------------------------------------|--------------------|--------|
| DPOR_PERI_CLK_EN_REG                     | clock gate for peripherals                                                                    | 0x3FF0001C         | R/W    |
| DPOR_PERI_RST_EN_REG                     | reset for peripherals                                                                         | 0x3FF00020         | R/W    |
| DPOR_PERIP_CLK_EN_REG                    | clock gate for peripherals                                                                    | 0x3FF000CO         | R/W    |
| DPOR_PERIP_RST_EN_REG                    | reset for peripherals                                                                         | 0x3FF000C4         | R/W    |
| DPOR_WIFI_CLK_EN_REG                     | clock gate for Wi-Fi                                                                          | 0x3FF000CC         | R/W    |
| DPOR_WIF_RST_EN_REG                      | reset for Wi-Fi                                                                              | 0x3FF000D0         | R/W    |

**MMU/MPU Access Exception Registers**

| Name                                      | Description                                                                                   | Address            | Access |
|-------------------------------------------|----------------------------------------------------------------------------------------------|--------------------|--------|
| DPOR_MEM_ACCESS_DBUGO_REG                | SRAM MMU exception flag                                                                       | 0x3FF003E8         | RO     |
| DPOR_MEM_ACCESS_DBG1_REG                 | SRAM MPU exception flag                                                                      | 0x3FF003EC         | RO     |
| DPOR_PRO_CACHE_DBUGO_REG                 | PRO CACHE MMU exception flag                                                                  | 0x3FF003FO         | RO     |
| DPOR_APP_CACHE_DBUGO_REG                 | APP CACHE MMU exception flag                                                                  | 0x3FF00418         | RO     |
| DPOR_MMU_ACCESS_ILLEGAL_INT_EN_REG        | SRAM MMU exception interrupt enable register                                                 | 0x3FF00598         | R/W    |
| DPOR_MPU_ACCESS_ILLEGAL_INT_EN_REG        | SRAM MPU exception interrupt enable register                                                  | 0x3FF0059C         | R/W    |
| DPOR_CACHE_ACCESS_ILLEGAL_INT_EN_REG      | CACHE MMU exception interrupt enable register                                                  | 0x3FF003A0         | R/W    |

**Section Title:**
12.5 Registers

**Body Text:**

The addresses in parenthesis besides register names are the register addresses relative to the DPORT base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 12.4 Register Summary.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)