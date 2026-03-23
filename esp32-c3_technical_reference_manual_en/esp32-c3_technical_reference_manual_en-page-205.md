

```markdown
| No.| Chapter| Source| Configuration Register| Bit| Status Register Name|
|----:|--------|-------|-------------------------|----:|----------------------|
| 31 | reserved| reserved| reserved| 31 |                      |
| 32 | Timer Group (TIMG)| TG_TO_INTR| INTERRUPT_COREO_TG_TO_INT_MAP_REG| 0 |                      |
| 33 | Timer Group (TIMG)| TG_WDT_INTR| INTERRUPT_COREO_TG_WDT_INT_MAP_REG| 1 |                      |
| 34 | Timer Group (TIMG)| TG1_TO_INTR| INTERRUPT_COREO_TG1_TO_INT_MAP_REG| 2 |                      |
| 35 | Timer Group (TIMG)| TG1_WDT_INTR| INTERRUPT_COREO_TG1_WDT_INT_MAP_REG| 3 |                      |
| 36 | reserved| reserved| reserved| 36 |                      |
| 37 | System Timer (SYSTIMER)| SYSTIMER_TARGET0_INTR| INTERRUPT_COREO_SYSTIMER_TARGET0_INT_MAP_REG| 5 |                      |
| 38 | System Timer (SYSTIMER)| SYSTIMER_TARGET1_INTR| INTERRUPT_COREO_SYSTIMER_TARGET1_INT_MAP_REG| 6 |                      |
| 39 | System Timer (SYSTIMER)| SYSTIMER_TARGET2_INTR| INTERRUPT_COREO_SYSTIMER_TARGET2_INT_MAP_REG| 7 |                      |
| 40 | reserved| reserved| reserved| 8 |                      |
| 41 | reserved| reserved| reserved| 9 |                      |
| 42 | reserved| reserved| reserved| 10 |                     |
| 43 | On-Chip Sensor and Analog Signal Processing| vDIGITAL_ADC_INTR| INTERRUPT_COREO_APB_ADC_INT_MAP_REG| 11 |                     |
| 44 | GDMA Controller (GDMA)| GDMA_CHO_INTR| INTERRUPT_COREO_DMA_CHO_INT_MAP_REG| 12 |                     |
| 45 | GDMA Controller (GDMA)| GDMA_CH1_INTR| INTERRUPT_COREO_DMA_CH1_INT_MAP_REG| 13 | INTERRUPT_COREO_INTR_STATUS_1_REG |
| 46 | GDMA Controller (GDMA)| GDMA_CH2_INTR| INTERRUPT_COREO_DMA_CH2_INT_MAP_REG| 14 |                     |
| 47 | RSA Accelerator (RSA)| RSA_INTR| INTERRUPT_COREO_RSA_INTR_MAP_REG| 15 |                     |
| 48 | AES Accelerator (AES)| AES_INTR| INTERRUPT_COREO_AES_INTR_MAP_REG| 16 |                     |
| 49 | SHA Accelerator (SHA)| SHA_INTR| INTERRUPT_COREO_SHA_INTR_MAP_REG| 17 |                     |
| 50 | System Registers (SYSREG)| SW_INTR_0| INTERRUPT_COREO_CPU_INTR_FROM_CPU_0_MAP_REG| 18 |                     |
| 51 | System Registers (SYSREG)| SW_INTR_1| INTERRUPT_COREO_CPU_INTR_FROM_CPU_1_MAP_REG| 19 |                     |
| 52 | System Registers (SYSREG)| SW_INTR_2| INTERRUPT_COREO_CPU_INTR_FROM_CPU_2_MAP_REG| 20 |                     |
| 53 | System Registers (SYSREG)| SW_INTR_3| INTERRUPT_COREO_CPU_INTR_FROM_CPU_3_MAP_REG| 21 |                     |
| 54 | Debug Assistant (ASSIST_DEBUG)| ASSIST_DEBUG_INTR| INTERRUPT_COREO_ASSIST_DEBUG_INTR_MAP_REG| 22 |                     |
| 55 | Permission Control (PMS)| PMS_DMA_VIO_INTR| INTERRUPT_COREO_DMA_APBPERI_PMS_MONITOR_VIOLATE_INTR_MAP_REG| 23 |                     |
| 56 | Permission Control (PMS)| PMS_IBUS_VIO_INTR| INTERRUPT_COREO_CORE_O_IRAMO_PMS_MONITOR_VIOLATE_INTR_MAP_REG| 24 |                     |
| 57 | Permission Control (PMS)| PMS_DBUS_VIO_INTR| INTERRUPT_COREO_CORE_O_DRAMO_PMS_MONITOR_VIOLATE_INTR_MAP_REG| 25 |                     |
| 58 | Permission Control (PMS)| PMS_PERI_VIO_INTR| INTERRUPT_COREO_CORE_O_PIF_PMS_MONITOR_VIOLATE_INTR_MAP_REG| 26 |                     |
| 59 | Permission Control (PMS)| PMS_PERI_VIO_SIZE_INTR| INTERRUPT_COREO_CORE_O_PIF_PMS_MONITOR_VIOLATE_SIZE_INTR_MAP_REG| 27 |                     |
| 60 | reserved| reserved| reserved| 28 |                      |
```