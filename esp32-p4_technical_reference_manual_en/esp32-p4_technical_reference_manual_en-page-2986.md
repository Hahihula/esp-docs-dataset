

# 60.6 Register Summary

## 60.6.1 Interrupt and Status Register Summary

The addresses in this section are relative to Touch Sensor base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Interrupt Register** |  |  |  |
| RTC_TOUCH_INT_RAW_REG | Touch sensor interrupt raw register | 0x0000 | R/SS/WTC |
| RTC_TOUCH_INT_ST_REG | Touch sensor interrupt status register | 0x0004 | RO |
| RTC_TOUCH_INT_ENA_REG | Touch sensor interrupt enable register | 0x0008 | R/W |
| RTC_TOUCH_INT_CLR_REG | Touch sensor interrupt clear register | 0x000C | WT |
| **Status Register** |  |  |  |
| RTC_TOUCH_CHN_STATUS_REG | Scan mode status register | 0x0010 | RO |
| RTC_TOUCH_STATUS_1_REG | Touch pin 1 status register | 0x0018 | RO |
| RTC_TOUCH_STATUS_2_REG | Touch pin 2 status register | 0x001C | RO |
| RTC_TOUCH_STATUS_3_REG | Touch pin 3 status register | 0x0020 | RO |
| RTC_TOUCH_STATUS_4_REG | Touch pin 4 status register | 0x0024 | RO |
| RTC_TOUCH_STATUS_5_REG | Touch pin 5 status register | 0x0028 | RO |
| RTC_TOUCH_STATUS_6_REG | Touch pin 6 status register | 0x002C | RO |
| RTC_TOUCH_STATUS_7_REG | Touch pin 7 status register | 0x0030 | RO |
| RTC_TOUCH_STATUS_8_REG | Touch pin 8 status register | 0x0034 | RO |
| RTC_TOUCH_STATUS_9_REG | Touch pin 9 status register | 0x0038 | RO |
| RTC_TOUCH_STATUS_10_REG | Touch pin 10 status register | 0x003C | RO |
| RTC_TOUCH_STATUS_11_REG | Touch pin 11 status register | 0x0040 | RO |
| RTC_TOUCH_STATUS_12_REG | Touch pin 12 status register | 0x0044 | RO |
| RTC_TOUCH_STATUS_13_REG | Touch pin 13 status register | 0x0048 | RO |
| RTC_TOUCH_STATUS_14_REG | Touch pin 14 status register | 0x004C | RO |
| RTC_TOUCH_STATUS_15_REG | Sleep mode touch pin status register | 0x0050 | RO |