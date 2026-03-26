

# 61.8 Register Summary

The addresses in this section are relative to Temperature Sensor base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Control Registers** | | | |
| TSENS_CTRL_REG | Temperature sensor control register 1. | 0x0000 | varies |
| TSENS_CTRL2_REG | Temperature sensor control register 2. | 0x0004 | R/W |
| **Interrupt Registers** | | | |
| TSENS_INT_RAW_REG | Raw register of temperature sensor interrupt. | 0x0008 | R/WTC/SS |
| TSENS_INT_ST_REG | State register of temperature sensor interrupt. | 0x000C | RO |
| TSENS_INT_ENA_REG | Enable register of temperature sensor interrupt. | 0x0010 | R/WTC |
| TSENS_INT_CLR_REG | Clear register of temperature sensor interrupt. | 0x0014 | WT |
| TSENS_INT_ENA_W1TS_REG | TSENS_INT_ENA_REG configuration register | 0x001C | WT |
| TSENS_INT_ENA_W1TC_REG | TSENS_INT_ENA_REG configuration register | 0x0020 | WT |
| **Wake-up Control Registers** | | | |
| TSENS_WAKEUP_CTRL_REG | Temperature sensor wake-up control registers. | 0x0024 | varies |
| TSENS_SAMPLE_RATE_REG | Hardware automatic sampling control registers. | 0x0028 | R/W |