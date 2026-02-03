**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Section Header: Register 35.6, LEDC_CHn_DUTY_R_REG**

- **Description:** This register stores the current duty of output signal on channel n.
- **Register Address:** `0x100 + 0x14 * n`
- **Bit Description (from left to right):**
  - [31] (reserved)
  - ... (bits not specified in text)

**Section Header: Register 35.7, LEDC_TIMERx_CONF_REG**

- **Description:** This register is used to control the range of the counter in timer x.
- **Register Address:** `0xA0 + 0x8 * x`
- **Bit Description (from left to right):**
  - [31] ... [26]
    - LEDC_TIMERx_PAUSE
    - LEDC_TIMERx PARA_UP
    - LEDC_TIMERx_DUTY_RES.
  - [25]...[24]
    - Reserved bits not specified in text

**Section Header: Register 35.8, LEDC_TIMERx_VALUE_REG**

- **Description:** This register stores the current counter value of timer x.

**Bit Description (from left to right):**
- ... [14]...
  - LEDC_TIMERx_CNT
    - This bit is used for configuring the divisor for the divider in timer x.
    - The least significant eight bits represent the fractional part. 

**Additional Information:**
- **LEDC_TIMERx_DUTY_RES:** This register stores the current duty of output signal on channel n (RO).
- **LEDC_TIMERx_PAUSE:** This bit is used to suspend the counter in timer x (R/W)
- **LEDC_TIMERx_RST:** This bit is used to reset timer x. The counter will show 0 after reset.
- **LEDC_TIMERx PARA_UP:** Set this bit to update `LEDC_CLK_DIV_TIMER` and `LEDC_TIMERx_DUTY_RES`.
- **LEDC_TIMERx_CNT:** Stores the current counter value of timer x (RO).

**Footer:**
Espressif Systems
1322 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback