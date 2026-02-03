**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**GoBack Link:** GoBack

---

### Table of Contents:

#### Name | Description | Address | Access
- **LEDC_CH4_DUTY_R_REG**: Current duty cycle for channel 4 | 0x0060 | RO
- **LEDC_CH5_DUTY_R_REG**: Initial duty cycle for channel 5 | 0x006C | R/W
- **LEDC_CH5_DUTY_R_REG**: Current duty cycle for channel 5 | 0x0074 | RO
- **LEDC_CH6_DUTY_R_REG**: Initial duty cycle for channel 6 | 0x0080 | R/W
- **LEDC_CH6_DUTY_R_REG**: Current duty cycle for channel 6 | 0x0088 | RO
- **LEDC_CH7_DUTY_R_REG**: Initial duty cycle for channel 7 | 0x0094 | R/W
- **LEDC_CH7_DUTY_R_REG**: Current duty cycle for channel 7 | 0x009C | RO

#### Timer Register:
- **LEDC_TIMERO_CONF_REG**: Timer 0 configuration | 0x00A0 | varies
- **LEDC_TIMERO_VALUE_REG**: Timer 0 current counter value | 0x00A4 | RO
- **LEDC_TIMER1_CONF_REG**: Timer 1 configuration | 0x00A8 | varies
- **LEDC_TIMER1_VALUE_REG**: Timer 1 current counter value | 0x00AC | RO
- **LEDC_TIMER2_CONF_REG**: Timer 2 configuration | 0x00B0 | varies
- **LEDC_TIMER2_VALUE_REG**: Timer 2 current counter value | 0x00B4 | RO
- **LEDC_TIMER3_CONF_REG**: Timer 3 configuration | 0x00B8 | varies
- **LEDC_TIMER3_VALUE_REG**: Timer 3 current counter value | 0x00BC | RO

#### Interrupt Register:
- **LEDC_INT_RAW_REG**: Raw interrupt status | 0x00C0 | RO
- **LEDC_INT_ST_REG**: Masked interrupt status | 0x00C4 | R/W
- **LEDC_INT_ENA_REG**: Interrupt enable bits | 0x00C8 | WO
- **LEDC_INT_CLR_REG**: Interrupt clear bits | 0x00CC | RO

#### Version Register:
- **LEDC_DATE_REG**: Version control register | 0x00FC | R/W

---

**Footer:**
Espressif Systems  
Page number: 1318  
Document version and title: ESP32-S3 TRM (Version 1.7)  
Link to submit documentation feedback