**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**

- The three PWM timer’s synchronization outputs.
- Three synchronization signals from the GPIO matrix: PWMn_SYNC0_IN, PWMn_SYNC1_IN, PWMn_SYNC2_IN.

No synchronization input signal selected

- Configure the source of the PWM timer's synchronization output to one of the four sources below:
  - Synchronization input signal
  - Event generated when value of the PWM timer is equal to zero
  - Event generated when value of the PWM timer is equal to period
  - Event generated when writing toggling value to MCPWM_TIMERx_SYNC_SW bit

- Configure the method of period updating.

**Subsection Title:**
36.3.1.3 Operator Submodule

**Diagram Description (Figure Caption):**
Figure 36.3-3. Operator Submodule
PWM_OPERATORx_TIMESEL -> operator x timer status -> PWMxA, PWMxB
timer 0 status -> fault event 0; timer 1 status -> fault event 1; timer 2 status -> fault event 2

**Additional Information:**
The configuration parameters of the operator submodule are shown in Table 36.3-1.

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)