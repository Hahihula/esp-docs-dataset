**Title:**
Chapter 28 LED PWM Controller (LEDC)

**Subtitles and Sections:**

1. **Register 28.17, LEDC_INT_ENA_REG (0x0188)**
   - Description:
     ```
     LEDC_DUTY_CHNG_END_LSCHn_INTENA The interrupt enable bit for the LEDC_DUTY_CHNG_END_LSCHn_INT interrupt.
     LEDC_DUTY_CHNG_END_HSCHn_INTENA The interrupt enable bit for the LEDC_DUTY_CHNG_END_HSCHn_INT interrupt.

     LEDC_LSTIMERx_OVF_INTENA The interrupt enable bit for the LEDC_LSTIMERx_OVF_INT interrupt. (R/W)

     LEDC_HSTIMERx_OVF_INTENA The interrupt enable bit for the LEDC_HSTIMERx_OVF_INT interrupt.
     ```

2. **Register 28.18, LEDC_INT_CLR_REG (0x018C)**
   - Description:
     ```
     LEDC_DUTY_CHNG_END_LSCHn_INTCLR Set this bit to clear the LEDC_DUTY_CHNG_END_LSCHn_INT interrupt.
     LEDC_DUTY_CHNG_END_HSCHn_INTCLR Set this bit to clear the LEDC_DUTY_CHNG_END_HSCHn_INT interrupt.

     LEDC_LSTIMERx_OVF_INTCLEAR Set this bit to clear the LEDC_LSTIMERx_OVF_INT interrupt. (WO)

     LEDC_HSTIMERx_OVF_INTCLEAR Set this bit to clear the LEDC_HSTIMERx_OVF_INT interrupt.
     ```

**Footer:**
- Espresso Systems
- ESP32 TRM (Version 5.6)
- Submit Documentation Feedback

**Navigation Link:** GoBack