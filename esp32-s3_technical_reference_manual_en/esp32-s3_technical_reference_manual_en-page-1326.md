**Chapter Title:**
Chapter 36

**Section Titles and Content:**

1. **Motor Control PWM (MCPWM) Overview**
   - The Motor Control Pulse Width Modulator (MCPWM) peripheral is intended for motor and power control.
   - It provides six PWM outputs that can be set up to operate in several topologies, including a pair of PWM outputs driving an H-bridge.

2. **Features:**

   Each MCPWM peripheral has one clock divider (prescaler), three PWM timers, three PWM operators, and a capture module:
   
   Figure 36.2-1 shows the submodules inside and the signals on the interface.
   - **PWM Timers O, 1 and 2**
     - Every PWM timer has a dedicated 8-bit clock prescaler.

   - The 16-bit counter in the PWM timer can work in count-up mode, count-down mode or count-up-down mode:
     - A hardware sync or software sync can trigger a reload on the PWM timer with a phase register. It will also trigger the prescaler’s restart.
   
   - **PWM Operators O, 1 and 2**
     - Every PWM operator has two PWM outputs: PWMxA and PWMxB.

3. **Additional Information about ESP32-S3:**
   - The timing and control resources inside are allocated into two major types of submodules:
     - PWM timers
     - Timers or external sources.
   
   Each PWM operator also contains a dedicated capture submodule that is used in systems where accurate timing of external events is important.

4. **Figure Reference (36.2-1):**
   - The figure shows the submodules inside and signals on the interface for each component described above, including details about clock prescalers, counter modes, sync mechanisms, etc.
   
5. **Submodule Function Overview:**
   - An overview of the submodules' function in Figure 36.2-1 is shown below:
     - PWM Timers O, 1 and 2
       - Every PWM timer has a dedicated clock prescaler.

**Footer Information:** 
- Espressif Systems | ESP32-S3 TRM (Version 1.7)