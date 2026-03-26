
```markdown
| Name                                       | Description                  | Address | Access |
|--------------------------------------------|------------------------------|---------|--------|
| RTC_TOUCH_STATUS_16_REG                    | Proximity mode status register | 0x0054  | RO     |
| RTC_TOUCH_STATUS_17_REG                    | Frequency hopping status register | 0x0058  | RO     |
| RTC_TOUCH_CHN_TMP_STATUS_REG               | Touch status register        | 0x005C  | RO     |
| Version Control Register                   |                              |         |        |
| RTC_TOUCH_DATE_REG                         | Version control register     | 0x0100  | R/W    |

## 60.6.2 Configuration Register Summary

The addresses in this section are relative to LP Analog Peripheral base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| Configuration Register                     |                                                                                                  |         |        |
| LP_ANA_TOUCH_APPROACH_WORK_MEAS_NUM_REG   | Configuration register for the number of measurements in proximity mode                           | 0x00FC  | R/W    |
| LP_ANA_TOUCH_SCAN_CTRL1_REG                | Scan mode configuration register 1                                                             | 0x0100  | R/W    |
| LP_ANA_TOUCH_SCAN_CTRL2_REG                | Scan mode configuration register 2                                                             | 0x0104  | R/W    |
| LP_ANA_TOUCH_WORK_REG                      | Sample preprocessing register                                                                  | 0x0108  | varies |
| LP_ANA_TOUCH_WORK_MEAS_NUM_REG             | Configuration register for number of measurements at different frequency modes                  | 0x010C  | R/W    |
| LP_ANA_TOUCH_FILTER1_REG                   | Touch detection configuration register 1                                                      | 0x0110  | R/W    |
| LP_ANA_TOUCH_FILTER2_REG                   | Touch detection configuration register 2                                                      | 0x0114  | R/W    |
| LP_ANA_TOUCH_FILTER3_REG                   | Touch detection configuration register 3                                                      | 0x0118  | varies |
| LP_ANA_TOUCH_SLPO_REG                      | Sleep mode configuration register 1                                                           | 0x011C  | varies |
| LP_ANA_TOUCH_SLP1_REG                      | Sleep mode configuration register 2                                                           | 0x0120  | R/W    |
| LP_ANA_TOUCH_CLR_REG                       | Status clear register                                                                           | 0x0124  | WT     |
| LP_ANA_TOUCH_APPROACH_REG                  | Proximity mode configuration register                                                          | 0x0128  | R/W    |
| LP_ANA_TOUCH_FREQ0_SCAN_PARA_REG           | Analog parameter configuration register for touch sensor for frequency mode 0                 | 0x012C  | R/W    |
| LP_ANA_TOUCH_FREQ1_SCAN_PARA_REG           | Analog parameter configuration register for touch sensor for frequency mode 1                 | 0x0130  | R/W    |
```