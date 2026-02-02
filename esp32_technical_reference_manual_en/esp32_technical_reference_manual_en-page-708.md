**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Register Information:**
Register 29.49, PWM_GEN2_A_REG (0x00c0)

**Table Description:**
The table shows the bits of register PWM_GEN2_A_REG with their corresponding descriptions and values.

- **Bits:** 31 to 0
- Each bit is labeled as follows:
  - PWM_GEN2_A_DT1, PWM_GEN2_A_DTO, PWM_GEN2_A_DTEB, etc.
  
**Descriptions:**
Each description explains the action of a specific bit when triggered by certain events.

- **PWM_GEN2_A_DT1:** Action on PWM2A triggered by event_t1 when the timer decreases. 0: no change; 1: low; 2: high; 3: toggle.
- **PWM_GEN2_A_DTO, PWM_GEN2_A_DTEB, etc.:** Actions related to PWM2A being triggered by events t0 or TEB (when the timer increases/decreases).

**Footer Information:**
Espressif Systems
Page number: 708
Document version: ESP32 TRM (Version 5.6)
Link for submitting documentation feedback.

**Navigation Link:** GoBack