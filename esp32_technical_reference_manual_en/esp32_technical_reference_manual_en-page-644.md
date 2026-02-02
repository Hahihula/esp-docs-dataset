**Title:**
Chapter 28 LED PWM Controller (LEDC)

**Subtitles and Sections:**

1. **Register 28.15. LEDC_INT_RAW_REG (0x0180)**
   - Description of the register bits:
     - `LED_DUTY_CHNG_END_LSCHn_INT_RAW`: The raw interrupt status bit for the `LEDC_DUTY_CHNG_END_LSCHn_INT` interrupt.
     - `LED_DUTY_CHNG_END_HSCHn_INT_RAW`: The raw interrupt status bit for the `LEDC_DUTY_CHNG_END_HSCHn_INT` interrupt.

2. **Register 28.16. LEDC_INT_ST_REG (0x0184)**
   - Description of the register bits:
     - `LED_DUTY_CHNG_END_LSCHn_INT_ST`: The masked interrupt status bit for the `LEDC_DUTY_CHNG_END_LSCHn_INT` interrupt.
     - `LED_DUTY_CHNG_END_HSCHn_INT_ST`: The masked interrupt status bit for the `LEDC_DUTY_CHNG_END_HSCHn_INT` interrupt.

**Footer:**
- "Espressif Systems"
- Page number and document version:
  - "644 ESP32 TRM (Version 5.6)"
- Feedback link:
  - "Submit Documentation Feedback"