**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**Section Heading:**
12.2.3 Alarm Generation

**Body Text:**
A timer can be configured to trigger an alarm when the timer’s current value matches the alarm value. An alarm will cause an interrupt to occur and (optionally) an automatic reload of the timer's current value (see Section 12.2.4). The 54-bit alarm value is configured using TIMG_TxALARMLO_REG and TIMG_TxALARMHI_REG, which represent the lower 32-bits and higher 22-bits of the alarm value, respectively. However, the configured alarm value is ineffective until the alarm is enabled by setting the TIMG_Tx_ALARM_EN field. To avoid alarm being enabled “too late” (i.e., the timer value has already passed the alarm value when the alarm is enabled), the hardware will trigger the alarm immediately if the current timer value is higher than the alarm value (within a defined range) or lower, and within that time window of up-down counter increments. Table 12.2-1 and Table 12.2-2 show how these relationships between the current value of the timer, the alarm value, when an alarm occurs.

**Tables:**

- **Table Title:** Alarm Generation When Up-Down Counter Increments
  - Scenario | Range | Alarm
  - --- | --- | ---
  - 1 | ALARM_VALUE – TIMG_VALUE > 2^53 | Triggered
  - 2 | O < ALARM_VALUE – TIMG_VALUE ≤ 2^53 | Triggered when the up-down counter counts TIMG_VALUE up to ALARM_VALUE
  - 3 | O ≤ TIMG_VALUE – ALARM_VALUE < 2^53 | Triggered 
  - 4 | TIMG_VALUE – ALARM_VALUE ≥ 2^53 | Triggered

- **Table Title:** Alarm Generation When Up-Down Counter Decrements
  - Scenario | Range | Alarm
  - --- | --- | ---
  - 5 | TIMG_VALUE – ALARM_VALUE > 2^53 | Triggered
  - 6 | O < TIMG_VALUE – ALARM_VALUE ≤ 2^53 | Triggered when the up-down counter counts TIMG_VALUE down to ALARM_VALUE
  - 7 | O ≤ ALARM_VALUE – TIMG_VALUE < 2^53 | Triggered 
  - 8 | ALARM_VALUE – TIMG_VALUE ≥ 2^53 | Triggered

**Additional Information:**
When an alarm occurs, the TIMG_Tx_ALARM_EN field is automatically cleared and no alarm will occur again until the TIMG_Tx_ALARM_EN is set next time.

**Footer Text:** 
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)