**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Register Information:**
- **Register Name:** PWM_GENO_B_REG (0x0054)
- **Field Description Table:**

| Bit | Field           |
|-----|----------------|
| 31  | Reserved       |
| ... | ...            |
| 2   | PWM_GENO_BUTO |
| 1   | PWM_GENO_BUDEP|

**Action Descriptions for Each Register:**
- **PWM_GENO_B_DT1:** Action on PWMOB triggered by event_t1 when the timer decreases. (0: no change, 1: low, 2: high, 3: toggle.) (R/W)
- **PWM_GENO_B_DTO:** Action on PWMOB triggered by event_t0 when the timer decreases. (R/W)
- **PWM_GENO_B_DTEN:** Action on PWMOB triggered by event TEB when the timer decreases. (R/W)
- **PWM_GENO_B_TE:** Action on PWMOB triggered by event TEA when the timer increases. (R/W)
- **PWM_GENO_B_UT1:** Action on PWMOB triggered by event_t1 when the timer increases. (R/W)
- **PWM_GENO_BUTO:** Action on PWMOB triggered by event_t0 when the timer decreases. (R/W)
- **PWM_GENO_BUDEP:** Action on PWMOB triggered by event TEB when the timer increases. (R/W)
- **PWM_GENO_UTEN:** Action on PWMOB triggered by event TEA when the timer increases. (R/W)
- **PWM_GENO_UTEP:** Action on PWMOB triggered by event TEP when the timer decreases. (R/W)
- **PWM_GENO_UTTEP:** Action on PWMOB triggered by event TEZ when the timer increases. (R/W)

**Footer:**
Espressif Systems
691 ESP32 TRM (Version 5.6)