**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Header:**
Register 36.22. MCPWM_GENO_B_REG (0x0054)

**Table:**
- The table lists various registers with their bit positions and descriptions.
- Bits are labeled from "31" to "0".
- Each register is described as follows:
  - **MCPWM_GENO_B_UTEZ:** Action on PWMOB triggered by event TEZ when timer increasing. (R/W)
  - **MCPWM_GENO_B_UTEP:** Action on PWMOB triggered by event TEP when timer increasing.
  - **MCPWM_GENO_B_UTEA:** Action on PWMOB triggered by event TFA when timer increasing.
  - **MCPWM_GENO_B_UTEB:** Action on PWMOB triggered by event TEB when timer increasing. (R/W)
  - **MCPWM_GENO_BUTO:** Action on PWMOB triggered by event_t0 when timer increasing, decreasing or toggling state is not specified in the provided text.
  - **MCPWM_GENO_B_UT1:** Action on PWMOB triggered by event_t1 when timer increasing. (R/W)
  - **MCPWM_GENO_B_DTEZ:** Action on PWMOB triggered by event TEZ when timer decreasing, toggling state is not specified in the provided text.
  - **MCPWM_GENO_B_DTEP:** Action on PWMOB triggered by event TEP when timer decreasing. (R/W)
  - **MCPWM_GENO_B_DTEA:** Action on PWMOB triggered by event TEA when timer decreasing, toggling state is not specified in the provided text.
  - **MCPWM_GENO_B_DTEB:** Action on PWMOB triggered by event TEB when timer decreasing. (R/W)
  - **MCPWM_GENO_B_DTO:** Action on PWMOB triggered by event_t0 when timer decreasing, toggling state is not specified in the provided text.
  - **MCPWM_GENO_B_DT1:** Action on PWMOB triggered by event_t1 when timer decreasing. (R/W)

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback