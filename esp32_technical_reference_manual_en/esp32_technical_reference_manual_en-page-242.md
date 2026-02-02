**Chapter 12 DPort Registers**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| DPORT_APP_EFUSE_INT_MAP_REG | interrupt map | 0x3FF002C8 | R/W |
| DPORT_APP_TWI_INT_MAP_REG | interrupt map | 0x3FF002CC | R/W |
| DPORT_APP_RTC_CORE_INTR_MAP_REG | interrupt map | 0x3FF002D0 | R/W |
| DPORT_APP_RMT_INTR_MAP_REG | interrupt map | 0x3FF002D4 | R/W |
| DPORT_APP_PCNT_INTR_MAP_REG | interrupt map | 0x3FF002D8 | R/W |
| DPORT_APP_I2C_EXTO_INTR_MAP_REG | interrupt map | 0x3FF002DC | R/W |
| DPORT_APP_I2C_EXTI_INTR_MAP_REG | interrupt map | 0x3FF002E0 | R/W |
| DPORT_APP_RSA_INTRA_INTP_MAP_REG | interrupt map | 0x3FF002E4 | R/W |
| DPORT_APP_SPI1_DMA_INT_MAP_REG | interrupt map | 0x3FF002E8 | R/W |
| DPORT_APP_SPI2_DMA_INT_MAP_REG | interrupt map | 0x3FF002EC | R/W |
| DPORT_APP_SPI3_DMA_INT_MAP_REG | interrupt map | 0x3FF002F0 | R/W |
| DPORT_APP_WDG_INT_MAP_REG | interrupt map | 0x3FF002F4 | R/W |
| DPORT_APP_TIMER1_INT_MAP_REG | interrupt map | 0x3FF002F8 | R/W |
| DPORT_APP_TIMER2_INT_MAP_REG | interrupt map | 0x3FF002FC | R/W |
| DPORT_APP_TG_TO_EDGE_INT_MAP_REG | interrupt map | 0x3FF00300 | R/W |
| DPORT_APP_TG_T1_EDGE_INT_MAP_REG | interrupt map | 0x3FF00304 | R/W |
| DPORT_APP_TG_WDT_EDGE_INT_MAP_REG | interrupt map | 0x3FF00308 | R/W |
| DPORT_APP_TG_LACT_EDGE_INT_MAP_REG | interrupt map | 0x3FF0030C | R/W |
| DPORT_APP_TG1_TO_EDGE_INT_MAP_REG | interrupt map | 0x3FF00310 | R/W |
| DPORT_APP_TG1W2D EDGE_INT_MAP_REG | interrupt map | 0x3FF00314 | R/W |
| DPORT_APP_TG1W2D EDGE_INT_MAP_REG | interrupt map | 0x3FF00318 | R/W |
| DPORT_APP_MPU_IA_INTP_MAP_REG | interrupt map | 0x3FF0031C | R/W |
| DPORT_APP_CACHE_IA_INTP_MAP_REG | interrupt map | 0x3FF00320 | R/W |
| DPORT_APP_CACHE_IA_INTP_MAP_REG | interrupt map | 0x3FF00324 | R/W |
| DPORT_APP_CACHE_IA_INTP_MAP_REG | interrupt map | 0x3FF00328 | R/W |

---

**DMA registers**

- **DPORT_SPI_DMA_CHAN_SEL_REG**: selects DMA channel for SPI1, SPI2, and SPI3
  - Address: 0x3FF005A8
  - Access: R/W

---

**MPU/MMU registers**

- **DPORT_PRO_CACHE_CTRL_REG**: determines the virtual address mode of the external SRAM
  - Address: 0x3FF00040
  - Access: R/W
- **DPORT_PRO_CACHE_CTRL1_REG**: PRO cache MMU configuration
  - Address: 0x3FF00044
  - Access: R/W
- **DPORT_APP_CACHE_CTRL_REG**: determines the virtual address mode of the external SRAM
  - Address: 0x3FF00058
  - Access: R/W
- **DPORT_APP_CACHE_CTRL1_REG**: APP cache MMU configuration
  - Address: 0x3FF0005C
  - Access: R/W

---

**MMU registers**

- **DPORT_IMMU_PAGE_MODE_REG**: page size in the MMU for the internal SRAM O
  - Address: 0x3FF00080
  - Access: R/W
- **DPORT_DMMU_PAGE_MODE_REG**: page size in the MMU for the internal SRAM 2
  - Address: 0x3FF00084
  - Access: R/W

---

**MPU registers**

- **DPORT_AHB_MPU_TABLE_0_REG**: MPU for configuring DMA
  - Address: 0x3FF000B4
  - Access: R/W

---

*Espressif Systems*

*Page 242, ESP32 TRM (Version 5.6)*