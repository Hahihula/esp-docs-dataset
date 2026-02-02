**Chapter Title:**
Chapter 28 LED PWM Controller (LEDC)

**Section Titles and Content:**

1. **LED Duty Control Registers:**
   - `LEDC_DUTY_START_H/LSCHn`
   - `LEDC_DUTY_INC_H/LSCHn`
   - `LEDC_DUTY_NUM_H/LSCHn`
   - `LEDC_DUTY_CYCLE_H/LSCHn`
   - `LEDC_DUTY_SCALE_H/LSCHn`

2. **Interrupt Configuration:**
   - Configure the second fade only after `LEDC_DUTY_CHNG_END_HSCHn` or `LEDC_DUTY_CHNG_END_LSCHn` interrupt is generated.
   - When LEDC is in decremental fade mode and `LEDC_DUTY_HSCHn` cannot be set to 1. Similarly, when LEDC is in decremental fade mode and `LEDC_DUTY_LSC_H` or `LEDC_DUTY_SCALE_HSCHn` (or `LEDC_DUTY SCALE_LSCHn`) cannot be set to 1.

3. **Interrupts:**
   - `LEDC_DUTY_CHNG_END_LSCHn_INT`: Triggered when a fade on low-speed channel has finished.
   - `LEDC_DUTY_CHNG_END_HSCHn_INT`: Triggered when a fade on high-speed channel has finished.
   - `LEDC_HS_TIMERx_OVF_INT`: Triggered when the high-speed timer reaches its maximum counter value (where x is 1 to 5).
   - `LEDC_LS_TIMERx_OVF_INT`: Triggered when low-speed timer reaches its maximum counter value.

4. **Register Summary:**
   - The addresses in this section are relative to LED PWM base address provided in Table 3.3-6.
   - Abbreviations given for columns:
     - Access Types (Access): `R/W` or `R`

5. **Configuration Registers with Details and Addresses:** 
   | Name                   | Description                                    | Address            | Access |
   |------------------------|-------------------------------------------------|--------------------|--------|
   | LEDC_CONF_REG         | Global ledc configuration register              | 0x3FF59190        | R/W    |
   | LEDC_HSCH0_CONFO_REG  | Configuration register O for high-speed channel 0| 0x3FF59000        | R/W    |
   | LEDC_HSCH1_CONFO_REG  | Configuration register O for high-speed channel 1| 0x3FF59014        | R/W    |
   | LEDC_HSCH2_CONFO_REG  | Configuration register O for high-speed channel 2| 0x3FF59028        | R/W    |
   | LEDC_HSCH3_CONFO_REG  | Configuration register O for high-speed channel 3| 0x3FF5903C        | R/W    |
   | LEDC_HSCH4_CONFO_REG  | Configuration register O for high-speed channel 4| 0x3FF59050        | R/W    |
   | LEDC_HSCH5_CONFO_REG  | Configuration register O for high-speed channel 5| 0x3FF59064        | R/W    |

**Footer:**
- Page number and document version information:
  - "Espressif Systems"
  - "ESP32 TRM (Version 5.6)"
  - "Submit Documentation Feedback"