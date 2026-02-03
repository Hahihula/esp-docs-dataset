**Title:**
Chapter 35 LED PWM Controller (LEDC)

**Subtitles and Sections:**

1. **Register 35.11. LEDC_INT_ENA_REG (0x00C8)**
   - Description:
     ```
     LEDC_TIMERx_OVF_INT_ENA The interrupt enable bit for the LEDC_TIMERx_OVF_INT interrupt.
     (R/W)
     ```
   - Bit Positions and Labels: 
     ```
     31 reserved
     29-20 LEDC_DUTY_CHGEnd_ENA
     17-8 Reserved bits
     7-4 LEDC_DUTY_CHGEnd_INT_ENA
     3-2 LEDC_DUTY_CHGEnd_INT
     1 LEDC_TIMERx_OVF_INT
     0 Reset
     ```

   - Description:
     ```
     LEDC_DUTY_CHNG_END INT ENA The interrupt enable bit for the LEDC_DUTY_CHNG_END INT interrupt.
     (R/W)
     ```
   - Bit Positions and Labels: 
     ```
     31 reserved
     29-0 Reserved bits
     ```

   - Description:
     ```
     LEDC_DUTY_CHNGEnd_CNT_CHn_INT_ENA The interrupt enable bit for the LEDC_OVF_CNT_CHn INT interrupt.
     (R/W)
     ```
   - Bit Positions and Labels: 
     ```
     31 reserved
     29-0 Reserved bits
     ```

2. **Register 35.12. LEDC_INT_CLR_REG (0x00CC)**
   - Description:
     ```
     LEDC_TIMERx_OVF_INT_CLR Set this bit to clear the LEDC_TIMERx OVF INT interrupt.
     (WO)
     ```
   - Bit Positions and Labels: 
     ```
     31 reserved
     29-20 Reserved bits
     17-8 Reserved bits
     7-4 LEDC_DUTY_CHGEnd_INT_CLR
     3-2 LEDC_DUTY_CHGEnd_INT
     1 LEDC_TIMERx_OVF_INT
     0 Reset
     ```

   - Description:
     ```
     LEDC_DUTY_CHNG_END_CNT_CHn_INT_CLR Set this bit to clear the LEDC_DUTY_CHNG_END CHn INT interrupt.
     (WO)
     ```
   - Bit Positions and Labels: 
     ```
     31 reserved
     29-0 Reserved bits
     ```

   - Description:
     ```
     LEDC_OVF_CNT_CHn_INT_CLR Set this bit to clear the LEDC_OVF_CNT_CHn INT interrupt.
     (WO)
     ```
   - Bit Positions and Labels: 
     ```
     31 reserved
     29-0 Reserved bits
     ```

**Footer Information:**
Espressif Systems  
Page number: 1324  
Document version: ESP32-S3 TRM (Version 1.7)  
Link to submit documentation feedback.

**Navigation Link:** GoBack