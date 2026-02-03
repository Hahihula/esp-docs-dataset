**Title: Chapter 9 Interrupt Matrix (INTERRUPT)**

**Table Columns:**  
- Name  
- Description  
- Address  
- Access  

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| INTERRUPT_CORE1_RSA_INT_MAP_REG | RSA interrupt configuration register | 0x0930 | R/W |
| INTERRUPT_CORE1_AES_INT_MAP_REG | AES interrupt configuration register | 0x0934 | R/W |
| INTERRUPT_CORE1_SHA_INT_MAP_REG | SHA interrupt configuration register | 0x0938 | R/W |
| INTERRUPT_CORE1_CPU_INTR_FROM_CPU_0_MAP_REG | CPU_INTR_FROM_CPU_0 interrupt configuration register | 0x093C | R/W |
| INTERRUPT_CORE1_CPU_INTR_FROM_CPU_1_MAP_REG | CPU_INTR_FROM_CPU_1 interrupt configuration register | 0x0940 | R/W |
| INTERRUPT_CORE1_CPU_INTR_FROM_CPU_2_MAP_REG | CPU_INTR_FROM_CPU_2 interrupt configuration register | 0x0944 | R/W |
| INTERRUPT CORE1_CPU_INTR FROM CPU_3_MAP_REG | CPU_INTR_FROM_CPU_3 interrupt configuration register | 0x0948 | R/W |
| INTERRUPT CORE1_DMA_APBPERI_PMS_MONITOR_VIOLATE_INTR_MAP_REG | dma_pms_monitor_violatile interrupt configuration register | 0x0950 | R/W |
| INTERRUPT CORE1_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core0_IRam0_pms_monitor_violatile interrupt configuration register | 0x0954 | R/W |
| INTERRUPT CORE1_CORE_0_DRAMO_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core0_DRam0_pms_monitor_violatile interrupt configuration register | 0x0958 | R/W |
| INTERRUPT CORE1_CORE_0_PIFF_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core0_PIFF_pms_monitor_violatile interrupt configuration register | 0x095C | R/W |
| INTERRUPT CORE1 CORE_0_PIFF_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core0_PIFF_pms_monitor_violatile_size_interrupt configuration register | 0x0960 | R/W |
| SIZEINTR_MAP_REG | size_interrupt_map_register | 0x0964 | R/W |
| INTERRUPT CORE1 CORE_1_IRAMO_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core1_IRam0_pms_monitor_violatile interrupt configuration register | 0x0968 | R/W |
| INTERRUPT CORE1 CORE_1_DRAMO_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core1_DRam0_pms_monitor_violatile interrupt configuration register | 0x0970 | R/W |
| INTERRUPT CORE1 CORE_1_PIFF_PMS_MONITOR_VIOLATE_INTR_MAP_REG | core1_PIFF_pms_monitor_violatile interrupt configuration register | 0x0974 | R/W |
| INTERRUPT CORE1_CACHE_COREO_ACS_INT_MAP_REG | CACHE_COREO_ACS interrupt configuration register REG | 0x0978 | R/W |
| INTERRUPT CORE1_CACHE CORE_1_ACS_INT_MAP_REG | CACHE_CORE1_ACS interrupt configuration register REG | 0x097C | R/W |

**Footer:**  
- ESP32-S3 TRM (Version 1.7)