

# 39.8 Register Summary

The addresses in this section are relative to Temperature Sensor base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers** | | | |
| APB_SARADC_INT_ENA_REG | Enable register of SAR ADC and temperature sensor interrupts | 0x0040 | R/W |
| APB_SARADC_INT_RAW_REG | Raw register of SAR ADC and temperature sensor interrupts | 0x0044 | R/WTC/SS |
| APB_SARADC_INT_ST_REG | State register of SAR ADC and temperature sensor interrupts | 0x0048 | RO |
| APB_SARADC_INT_CLR_REG | Clear register of SAR ADC and temperature sensor interrupts | 0x004C | WT |
| APB_SARADC_APB_TSENS_CTRL_REG | Temperature sensor control register 1 | 0x0058 | varies |
| APB_SARADC_APB_TSENS_CTRL2_REG | Temperature sensor control register 2 | 0x005C | R/W |
| APB_TSENS_WAKE_REG | Temperature sensor wake-up mode configuration register | 0x0064 | varies |
| APB_TSENS_SAMPLE_REG | Temperature sensor configuration register | 0x0068 | R/W |
| **Version Control Register** | | | |
| APB_SARADC_CTRL_DATE_REG | Version control register | 0x03FC | R/W |