**Title: Chapter 39 On-Chip Sensors and Analog Signal Processing**

---

**Table of Registers Information**
- **Name**: APB_SARADC_DMA_CONF_REG, APB_SARADC_APB_ADC_CLKM_CONF, Status register, interrupt register, Version register

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| APB_SARADC_DMA_CONF_REG | DMA configuration register for SAR ADC | 0x006C | R/W |
| APB_SARADC_APB_ADC_CLKM_CONF | Configure SAR ADC clock | 0x0070 | R/W |
| Status register | Get SAR ADC1 sample data, Get SAR ADC2 sample data | APB_SARADC_APB_SARADC1_DATA_, APB_SARADC_APB_SARADC2_DATA_ | 0x0040 RO, 0x0078 RO |
| interrupt register | Enable SAR ADC interrupts, SAR ADC interrupt raw bits, SAR ADC interrupt status, Clear SAR ADC interrupts | APB_SARADC_INT_ENA_REG, APB_SARADC_INT_RAW_REG, APB_SARADC_INT_ST_REG, APB_SARADC_INT_CLR_REG | 0x005C R/W, 0x0060 RO, 0x0064 RO, 0x0068 WO |
| Version register | Version control register | APB_SARADC_APB_CTRL_DATE_REG | 0x03FC R/W |

---

**Section: Registers**

**Subsection Title: 39.7 Registers**

**Subsection Subtitle: 39.7.1 SENSOR (ALWAYS_ON) Registers**

The addresses in this section are relative to the [Low Power Management] base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Register Description**: RTC_CNTL_TOUCH_CTRL1_REG (0x0108)

| Offset | Register Name | Description |
|--------|---------------|-------------|
| 0x1000 | RTC_CNTL_TOUCH_MEA_NUM | Set sleep cycles for touch timer. Clock: RTC_SLOW_CLK. (R/W) |
| 0x1000 | RTC_CNTL_TOUCH_SLEEP_CYCLES | Configure measurement duration expressed in number of charge/discharge cycles. (R/W) |

---

**Footer**: Espressif Systems, ESP32-S3 TRM (Version 1.7), Submit Documentation Feedback