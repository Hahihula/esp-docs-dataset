**Title: Chapter 35 LED PWM Controller (LEDC)**

**GoBack**

---

### Register 35.9, LEDC_INT_RAW_REG (0x00CO)

| 31 | 20-19 | 18-17 | 16-15 | 14-13 | 12-11 | 10-9 | 8-7 | 6-5 | 4-3 | 2-1 |
|----|-------|-------|-------|-------|-------|------|-----|-----|-----|-----|
| (reserved) | LEDC_OVF_CNT_CHn_INT_RAW | ... | ... | ... | ... | ... | ... | ... | ... |

**LEDCC_TIMERx_OVF_INT_RAW**: Triggered when the timerx has reached its maximum counter value.  
(RO)

**LEDCC_DUTY_CHNG_END_CHn_INT_RAW**: Interrupt raw bit for channel n, triggered when the gradual change of duty has finished.  
(RO)

**LEDCC_OVF_CNT_CHn_INT_RAW**: Interrupt raw bit for channel n, triggered when the ovf_cnt has reached the value specified by LEDC_OVF_NUM_CHn.  
(RO)

---

### Register 35.10, LEDC_INT_ST_REG (0x00C4)

| 31 | 20-19 | 18-17 | ... |
|----|-------|-------|-----|
| (reserved) | LEDC_OVF_CNT_CHn_INT_ST | ... |

**LEDCC_TIMERx_OVF_INT_ST**: This is the masked interrupt status bit for the LEDC_TIMERx_OVF_INT_ENA.  
(RO)

**LEDCC_DUTY_CHNG_END_CHn_INT_ST**: This is the masked interrupt status bit for the LEDC_DUTY_CHNG_END_CHn_INT when LEDC_DUTY_CHNG_END_CHn_ENAIS set to 1.  
(RO)

**LEDCC_OVF_CNT_CHn_INT_ST**: This is the masked interrupt status bit for the LEDC_OVF_CNT_CHn_INT when LEDC_OVF_CNT_CHn_ENA is set to 1.  
(RO)

---

Espressif Systems

Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)