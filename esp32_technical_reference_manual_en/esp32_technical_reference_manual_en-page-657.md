**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description with Labels and Captions:**
- **Labels:** Period = 6, Direction, Decrease, Increase.
- Diagram shows a step waveform labeled as "PWM timer" indicating the steps from DTEP to UTEZ.

**Figure Caption:**
Figure 29.3-12. DTEP and UTEZ Generation in Count-Up/Down Mode

**Body Text with Annotations (using markdown syntax for emphasis):**

Please note that in the **Count-Up-Down Mode**, when the counting direction is increasing, the timer range is [0, period value - 1], and when the counting direction is decreasing, the timer range is [period value, 1]. That is, in this mode, when synchronizing the timer to 0, decreasing count direction will be illegal, namely,

**MCPWM_TIMERn_PHASE_DIRECTION cannot be set to 1.**

Similarly, when synchronizing the timer to period value, increasing counting direction will be illegal, namely,
**MCPWM_TIMERn_PHASE_DIRECTION cannot be set to 0.**

Therefore, when the timer is synchronized to 0, the counting direction can only be increasing, and

**MCPWM_TIMERn_PHASE_DIRECTION will be 0.**

When the timer is synchronized to the period value, the counting direction can only be decreasing,

and **MCPWM_TIMERn_PHASE_DIRECTION will be 1.**

---

**Subtitle:**
29.3.2.3 PWM Timer Shadow Register

**Body Text with Annotations (using markdown syntax for emphasis):**

The PWM timer’s period register and the PWM timer's clock prescaler register have shadow registers.

- **Purpose of a shadow register:** to save a copy of the value to be written into the active register at a specific moment synchronized with the hardware. Both register types are defined as follows:

  - **Active Register**
    This register is directly responsible for controlling all actions performed by hardware.
  
  - **Shadow Register**
    It acts as a temporary buffer for a value to be written on the active register.

Before this happens, the content of the shadow register has no direct effect on the controlled hardware. At a specific user-configured point in time,

the value saved in the shadow register is copied to the active register.
This helps to prevent spurious operation of the hardware, which may happen when a register is asynchronously modified by software.

Both the shadow register and the active register have the same memory address. The software always writes into, or reads from the shadow register. 

**Footer:**
Espressif Systems
657

**Link Texts:**
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)