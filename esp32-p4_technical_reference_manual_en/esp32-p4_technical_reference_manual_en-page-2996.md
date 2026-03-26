
```markdown
Register 60.9. RTC_TOUCH_STATUS_17_REG (0x0058)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| 30  | RTC_FREQ_SCAN_CNT           | Indicates the SCAN_CNT value of the current touch pin. (RO)                 |
| 29  | RTC_TOUCH_DBIAS              | Indicates the DBIAS value of the current touch pin. (RO)                     |
| 28  | RTC_TOUCH_DRV_HS            | Indicates the DRV_HS value of the current touch pin. (RO)                    |
| 27  | RTC_TOUCH_DRV_LS            | Indicates the DRV_LS value of the current touch pin. (RO)                    |
| 26  | RTC_TOUCH_DRES_LP_F         | Indicates the DRES_LP value of the current touch pin. (RO)                   |
| 25  | RTC_TOUCH_DCAP_LP_F         | Indicates the DCAP_LP value of the current touch pin. (RO)                   |

RTC_TOUCH_DCAP_LP_F Indicates the DCAP_LP value of the current touch pin. (RO)
RTC_TOUCH_DRES_LP_F Indicates the DRES_LP value of the current touch pin. (RO)
RTC_TOUCH_DRV_LS Indicates the DRV_LS value of the current touch pin. (RO)
RTC_TOUCH_DRV_HS Indicates the DRV_HS value of the current touch pin. (RO)
RTC_TOUCH_DBIAS Indicates the DBIAS value of the current touch pin. (RO)
RTC_FREQ_SCAN_CNT Indicates the SCAN_CNT value of the current touch pin. (RO)

Register 60.10. RTC_TOUCH_CHN_TMP_STATUS_REG (0x005C)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| 30  | RTC_TOUCH_PAD_INACTIVE_STATUS | Indicates whether the touch pin detects the touch pad from being touched to being released. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.<br>0: Touch release detected<br>1: Touch release not detected (RO) |
| 29  | RTC_TOUCH_PAD_ACTIVE_STATUS | Indicates whether the touch pin detects the process of being touched. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.<br>0: Touch detected<br>1: Touch not detected (RO) |

```