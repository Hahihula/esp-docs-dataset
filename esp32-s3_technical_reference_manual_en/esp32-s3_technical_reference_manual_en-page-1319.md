**Title:**
Chapter 35 LED PWM Controller (LEDC)

**Subtitle:**
35.5 Registers

**Body Text:**

The addresses in this section are relative to **LED PWM Controller** base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Title:**  
Register 35.1. LEDC_CHn_CONF0_REG (n: 0-7) (0x0000+0x14*n)

| Bits | Description |
|-------|-------------|
| 31    | (reserved) |
| ...   | ...         |
| 2     | LEDC_OVF_CNT_RESET_ST_CHn |
| 1     | LEDC_OVF_CNT_EN_CHn |
| ...   | ...         |
| 0     | Reset |

**Field Descriptions:**

- **LEDC_TIMER_SEL_CHn:** This field is used to select one of the timers for channel n.
  - `0`: select timer0
  - `1`: select timer1
  - `2`: select timer2
  - `3`: select timer3 (R/W)

- **LEDC_SIG_OUT_EN_CHn:** Set this bit to enable signal output on channel n. (R/W)
  
- **LEDC_IDLE_LV_CHn:** This bit is used to control the output value when channel n is inactive (when LEDC_SIG_OUT_EN_CHn is 0). (R/W)

- **LEDC_PARA_UP_CHn:** This bit is used to update the listed fields below for channel n, and will be automatically cleared by hardware. (WO)
  - `LEDC_HPOINT_CHn`
  - `LEDC_DUTY_START_CHn`
  - `LEDC_SIG_OUT_EN_CHn`
  - `LEDC_TIMER_SEL_CHn`
  - `LEDC_DUTY_NUM_CHn`
  - `LEDC_DUTY_CYCLE_CHn`
  - `LEDC_DUTY_SCALE_CHn`
  - `LEDC_DUTY_INC_CHn`
  - `LEDC_OVF_CNT_EN_CHn`

**Footer:**
Continued on the next page...

**Page Information:**  
Espressif Systems, Page number: 1319, Document version: ESP32-S3 TRM (Version 1.7)