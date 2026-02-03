**Title: Chapter 36 Motor Control PWM (MCPWM)**

**Subtitle: Register 36.50, MCPWM_GEN2_A_REG (0x00CO)**

**Binary Table Description**
- The table shows the binary representation of various registers in the MCPWM_GEN2_A_REG register.

**Body Text with Descriptions**

1. **MCPWM_GEN2_A_UTEZ**
   - Action on PWM2A triggered by event TEZ when timer increasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

2. **MCPWM_GEN2_A_UTEP**
   - Action on PWM2A triggered by event TEP when timer increasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

3. **MCPWM_GEN2_A_UTEA**
   - Action on PWM2A triggered by event TEA when timer increasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

4. **MCPWM_GEN2_A_UTEB**
   - Action on PWM2A triggered by event TEB when timer increasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

5. **MCPWM_GEN2_AUTO**
   - Action on PWM2A triggered by event_t0 when timer increasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

6. **MCPWM_GEN2AUTI**
   - Action on PWM2A triggered by event_t1 when timer increasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

7. **MCPWM_GEN2ADTEZ**
   - Action on PWM2A triggered by event TEZ when timer decreasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

8. **MCPWM_GEN2ADTEP**
   - Action on PWM2A triggered by event TEP when timer decreasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

9. **MCPWM_GEN2ADTEA**
   - Action on PWM2A triggered by event TEA when timer decreasing.
   - 0: no change, 1: low, 2: high
   - 3: toggle (R/W)

10. **MCPWM_GEN2ADTEB**
    - Action on PWM2A triggered by event TEB when timer decreasing.
    - 0: no change, 1: low, 2: high
    - 3: toggle (R/W)

11. **MCPWM_GEN2ADTO**
    - Action on PWM2A triggered by event_t0 when timer decreasing.
    - 0: no change, 1: low, 2: high
    - 3: toggle (R/W)

12. **MCPWM_GEN2ADT1**
    - Action on PWM2A triggered by event_t1 when timer decreasing.
    - 0: no change, 1: low, 2: high
    - 3: toggle (R/W)

**Footer Information**

- Page number and document version:
  - "Espressif Systems"
  - "ESP32-S3 TRM (Version 1.7)"
  
- Navigation Links:
  - Submit Documentation Feedback

This text provides a detailed description of the various actions that can be triggered on PWM2A in response to different events, with specific settings for each action based on whether it is low or high and if toggling should occur when certain conditions are met (R/W indicates read/write access).