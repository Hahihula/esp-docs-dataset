**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Titles and Content:**

1. **36.3.2.3 PWM Timer Shadow Register**
   - The text explains that the PWM timer’s period register, clock prescaler register have shadow registers for specific purposes:
     - Active Register
       - This is directly responsible for controlling all actions performed by hardware.
     - Shadow Register
       - Acts as a temporary buffer to store values before they are written into active. It saves user-configured points in time and copies the value from it back when needed, ensuring no direct effect on controlled hardware.

2. **36.3.2.4 PWM Timer Synchronization and Phase Locking**
   - Describes how PWM modules use a flexible synchronization method with each PWM timer having an input for synchronization output.
   - The synchronization can be selected through GPIO matrix signals or software, allowing the timers to chain together during phase locking.

3. **36.3.3 PWM Operator Submodule**
   - Lists functions of the PWM Operator submodule:
     - Generates a PWM signal pair based on timing references from corresponding PWM timer outputs.
     - Each output includes specific patterns for dead time and carrier superimposition if configured to do so under fault conditions.

**Figure Reference:**
- Figure 36.3-13 shows block diagram of the PWM operator (not displayed in text).

**Footer Information:**
- Page number: 1338
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Link:** 
- GoBack