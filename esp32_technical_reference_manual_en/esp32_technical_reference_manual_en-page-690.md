**Chapter Title:**
Motor Control PWM (MCPWM)

**Register Information:**
- Register Name: PWM_GENO_A_REG (0x0050)
- GoBack button

**Hexadecimal Memory Map for PWM_GENO_A:**

```
31 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1
| PWM_GENO_AUTO | PWM_GENOAUTOTEP | PWM_GENOAUTOTEZ |
| PWM_GENOAUTO | PWM_GENOAUTO | PWM_GENOAUTO |
```

**Description of Actions:**

- **PWM_GENO_A_DT1:** Action on PWMOA triggered by event_t1 when the timer decreases. 0: no change, 1: low, 2: high, 3: toggle. (R/W)
  
- **PWM_GENO_A_DT0:** Action on PWMOA triggered by event_t0 when the timer decreases. (R/W)

- **PWM_GENO_A_DTEB:** Action on PWMOA triggered by event TEB when the timer decreases. (R/W)

- **PWM_GENO_A_DTEA:** Action on PWMOA triggered by event TEA when the timer decreases. (R/W)

- **PWM_GENO_A_DTETEP:** Action on PWMOA triggered by event TEP when the timer decreases. (R/W)

- **PWM_GENO_A_DTETEZ:** Action on PWMOA triggered by event TEZ when the timer decreases. (R/W)

- **PWM_GENO_A_UT1:** Action on PWMOA triggered by event_t1 when the timer increases. (R/W)

- **PWM_GENO_AUTO:** Action on PWMOA triggered by event_t0 when the timer increases. (R/W)

- **PWM_GENOAUTOEB:** Action on PWMOA triggered by event TEB when the timer increases. (R/W)

- **PWM_GENOAUTEA:** Action on PWMOA triggered by event TEA when the timer increases. (R/W)

- **PWM_GENOAUTOEP:** Action on PWMOA triggered by event TEP when the timer increases. (R/W)

- **PWM_GENOAUTEZ:** Action on PWMOA triggered by event TEZ when the timer increases. (R/W)

**Footer:**
Espressif Systems
Page number 690, ESP32 TRM (Version 5.6)
Submit Documentation Feedback link