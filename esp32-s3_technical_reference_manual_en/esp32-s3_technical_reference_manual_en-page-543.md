**Title: Chapter 9 Interrupt Matrix (INTERRUPT)**

**Table Headers:**  
- No.  
- Source  
- Configuration Register  
- Status Register Bit  
- Name  

| No. | Source                                | Configuration Register                                                                                   | Status Register Bit | Name                                    |
|-----|---------------------------------------|--------------------------------------------------------------------------------------------------------|---------------------|-----------------------------------------|
| 72  | DMA_OUT_CH1_INT                       | INTERRUPT\Core_\_DMA_OUT_CH1_INT_MAP_REG                                                                | 8                   |                                          |
| 73  | DMA_OUT_CH2_INT                       | INTERRUPT\Core_\_DMA_OUT_CH2_INT_MAP_REG                                                                | 9                   |                                          |
| 74  | DMA_OUT_CH3_INT                       | INTERRUPT\Core_\_DMA_OUT_CH3_INT_MAP_REG                                                                | 10                  |                                          |
| 75  | DMA_OUT_CH4_INT                       | INTERRUPT\Core_\_DMA_OUT_CH4_INT_MAP_REG                                                                | 11                  |                                          |
| 76  | RSA_INR                               | INTERRUPT\Core_\_RSA_INR_MAP_REG                                                                      | 12                  |                                          |
| 77  | AES_INR                               | INTERRUPT\Core_\_AES_INR_MAP_REG                                                                      | 13                  |                                          |
| 78  | SHA_INR                               | INTERRUPT\Core_\_SHA_INR_MAP_REG                                                                      | 14                  |                                          |
| 79  | CPU_INR_FROM_CPU_0                   | INTERRUPT\Core_\_CPU_INR_FROM_CPU_0_MAP_REG                                                            | 15                  |                                          |
| 80  | CPU_INR_FROM_CPU_1                    | INTERRUPT\Core_\_CPU_INR_FROM_CPU_1_MAP_REG                                                            | 16                  |                                          |
| 81  | CPU_INR_FROM_CPU_2                    | INTERRUPT\Core_\_CPU_INR_FROM_CPU_2_MAP_REG                                                            | 17                  |                                          |
| 82  | CPU_INR_FROM_CPU_3                    | INTERRUPT\Core_\_CPU_INR_FROM_CPU_3_MAP_REG                                                            | 18                  |                                          |
|     | reserved                              | reserved                                                |                     |                                          |
| 84  | DMA_APB_PMS_MONITOR_VIOLATEINTR       | INTERRUPT\Core_\_DMA_APB_PMS_MONITOR_VIOLATE_INTR_MAP_REG                                               | 20                  | INTERRUPT\Core_\_INTR_STATUS_2_REG      |
| 85  | CORE_0_IRAMO_PMS_MONITOR_VIOLATEINTR | INTERRUPT\Core_\_IRAMO_PMS_MONITOR_VIOLATE_intr_MAP_REG                                                | 21                  |                                          |
| 86  | CORE_0_DRAMO_PMS_MONITOR_VIOLATEINTR | INTERRUPT\Core_\_DRAMO_PMS_MONITOR_VIOLATE_intr_MAP_REG                                                | 22                  |                                          |
| 87  | CORE_0_PIF_PMS_MONITOR_VIOLATEINTR    | INTERRUPT\Core_\_PIF_PMS_MONITOR_VIOLATE_intr_MAP_REG                                                  | 23                  |                                          |
| 88  | CORE_0_PIF_PMS_MONITOR_VIOLATE_SIZEINTR | INTERRUPT\Core_\_PIF_PMS_MONITOR_VIOLATE_SIZE_intr_MAP_REG                                             | 24                  |                                          |
| 89  | CORE_1_IRAMO_PMS_MONITOR_VIOLATEINTR   | INTERRUPT\Core_\_IRAMO_PMS_MONITOR_VIOLATE_intr_MAP_REG                                               | 25                  |                                          |
| 90  | CORE_1_DRAMO_PMS_MONITOR_VIOLATEINTR   | INTERRUPT\Core_\_DRAMO_PMS_MONITOR_VIOLATE_intr_MAP_REG                                               | 26                  |                                          |
| 91  | CORE_1_PIF_PMS_MONITOR_VIOLATEINTR     | INTERRUPT\Core_\_PIF_PMS_MONITOR_VIOLATE_intr_MAP_REG                                                  | 27                  |                                          |
| 92  | CORE_1_PIF_PMS_MONITOR_VIOLATE_SIZEINTR | INTERRUPT\Core_\_PIF_PMS_MONITOR_VIOLATE_SIZE_intr_MAP_REG                                             | 28                  |                                          |
| 93  | BACKUP_PMS_Violate_INT                | INTERRUPT\Core_\_BACKUP_PMS_Violate_map_REG                                                           | 29                  |                                          |
| 94  | CACHE_COREO_ACS_INR                   | INTERRUPT\Core_\_CACHE_COREO_ACS_MAP_REG                                                              | 30                  |                                          |
| 95  | CACHE_CORE1_ACS_INR                   | INTERRUPT\Core_\_CACHE_CORE1_ACS_MAP_REG                                                              | 31                  |                                          |
| 96  | USB_DEVICE_INT                        | INTERRUPT\Core_\_USB_DEVICE_INT_MAP_REG                                                                | 0                   |                                          |
| 97  | PERI_BACKUP_INT                       | INTERRUPT\Core_\_PERI_BACKUP_INT_MAP_REG                                                               | 1                   | INTERRUPT_Core_\_INTR_STATUS_3_REG      |
| 98  | DMA_EXTMEM_REJECT_INT                 | INTERRUPT\Core_\_DMA_EXTMEM_REJECT_INT_MAP_REG                                                        | 2                   |                                          |

**Footer:**  
- ESP32-S3 TRM (Version 1.7)