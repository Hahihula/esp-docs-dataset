**Title: Chapter 9 Interrupt Matrix (INTERRUPT)**

**Table Columns:**
- Name
- Description
- Address
- Access

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| INTERRUPT_CORE0_PWM0_INTR_MAP_REG | PWM0 interrupt configuration register | 0x007C | R/W |
| INTERRUPT_CORE0_PWM1_INTR_MAP_REG | PWM1 interrupt configuration register | 0x0080 | R/W |
| INTERRUPT_CORE0_LEDC_INT_MAP_REG | LEDC interrupt configuration register | 0x008C | R/W |
| INTERRUPT_CORE0_EFUSE_INT_MAP_REG | EFUSE interrupt configuration register | 0x0090 | R/W |
| INTERRUPT_CORE0_TWAI_INTP_MAP_REG | CAN interrupt configuration register | 0x0094 | R/W |
| INTERRUPT_CORE0_USB_INTP_MAP_REG | USB interrupt configuration register | 0x0098 | R/W |
| INTERRUPT CORE0_RTC_CORINT_INTP_MAP_REG | RTC_CORINT interrupt configuration register | 0x009C | R/W |
| INTERRUPT CORE0_RMT_INTP_MAP_REG | RMT interrupt configuration register | 0x00A0 | R/W |
| INTERRUPT CORE0_PCNT_INTP_MAP_REG | PCNT interrupt configuration register | 0x00A4 | R/W |
| INTERRUPT CORE0_I2C_EXTO_INTP_MAP_REG | I2C_EXTO interrupt configuration register | 0x00A8 | R/W |
| INTERRUPT CORE0_I2C_EXTI_INTP_MAP_REG | I2C_EXTI interrupt configuration register | 0x00AC | R/W |
| INTERRUPT CORE0_TG_TO_INT_MAP_REG | TG_TO interrupt configuration register | 0x00C8 | R/W |
| INTERRUPT CORE0_TG_T1_INTP_MAP_REG | TG_T1 interrupt configuration register | 0x00CC | R/W |
| INTERRUPT CORE0_TG_WDT_INTP_MAP_REG | TG_WDT interrupt configuration register | 0x00D0 | R/W |
| INTERRUPT CORE0_TG1_TO_INT_MAP_REG | TG1_TO interrupt configuration register | 0x00D4 | R/W |
| INTERRUPT CORE0_TG1_T1_INTP_MAP_REG | TG1_T1 interrupt configuration register | 0x00D8 | R/W |
| INTERRUPT CORE0_TG1_WDT_INTP_MAP_REG | TG1_WDT interrupt configuration register | 0x00DC | R/W |
| INTERRUPT CORE0_CACHE_IA_INTP_MAP_REG | CACHE_IA interrupt configuration register | 0x00E0 | R/W |
| INTERRUPT CORE0_SYSTIMER_TARGET0_INTP_MAP_REG | SYSTIMER_TARGET0 interrupt configuration register | 0x00E4 | R/W |
| INTERRUPT CORE0_SYSTIMER_TARGET1_INTP_MAP_REG | SYSTIMER_TARGET1 interrupt configuration register | 0x00E8 | R/W |
| INTERRUPT CORE0_SYSTIMER_TARGET2_INTP_MAP_REG | SYSTIMER_TARGET2 interrupt configuration register | 0x00EC | R/W |
| INTERRUPT CORE0_SPI_MEM_REJECT_INTP_MAP_REG | SPI_MEM_REJECT interrupt configuration register | 0x00F0 | R/W |
| INTERRUPT CORE0_DCACHE_PRELOAD_INTP_MAP_REG | DCACHE_PRELOAD interrupt configuration register | 0x00F4 | R/W |
| INTERRUPT CORE0_ICACHE_PRELOAD_INTP_MAP_REG | ICACHE_PRELOAD interrupt configuration register | 0x00F8 | R/W |
| INTERRUPT CORE0_DCACHE_SYNC_INTP_MAP_REG | DCACHE_SYNC interrupt configuration register | 0x00FC | R/W |
| INTERRUPT CORE0_ICACHE_SYNC_INTP_MAP_REG | ICACHE_SYNC interrupt configuration register | 0x0100 | R/W |
| INTERRUPT CORE0_APB_ADC_INTP_MAP_REG | APB_ADC interrupt configuration register | 0x0104 | R/W |
| INTERRUPT CORE0_DMA_IN_CHO_INTP_MAP_REG | DMA_IN_CHO interrupt configuration register | 0x0108 | R/W |
| INTERRUPT CORE0_DMA_IN_CH1_INTP_MAP_REG | DMA_IN_CH1 interrupt configuration register | 0x010C | R/W |

**Footer:**
- ESP32-S3 TRM (Version 1.7)