**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Title and Diagram:**
29.3.1.5 Capture Submodule

**Figure Caption:**
Figure 29.3-5. Capture Submodule

**Configuration Parameters List under "Capture Submodule":**
- Select the edge polarity and prescaling of the capture input.
- Set up a software-triggered capture.
- Configure the capture timer’s sync trigger and sync phase.

**Section Title with Description:**
29.3.2 PWM Timer Submodule
Each MCPWM module has three PWM timer submodules. Any of them can determine the necessary event timing for any of the three PWM operator submodules. Built-in synchronization logic allows multiple PWM timer submodules, in one or more MCPWM modules, to work together as a system, when using synchronization signals from the GPIO matrix.

**Subsection Title and Description:**
29.3.2.1 Configurations of the PWM Timer Submodule
Users can configure the following functions of the PWM timer submodule:
- Control how often events occur by specifying the PWM timer frequency or period.
- Configure a particular PWM timer to synchronize with other PWM timers or modules.

**List under "Configurations of the PWM Timer Submodule":**
- Get a PWM timer in phase with other PWM timers or modules. 
- Set one of the following timer counting modes: count-up, count-down, count-up-down.
- Change the rate of the PWM clock (PTyclk) with a prescaler. Each timer has its own prescaler configured with PWM_TIMERx PRESCALE of register PWM_TIMERO_CFGO_REG. The PWM timer increments or decrements at a slower pace, depending on the setting of this register.

**Subsection Title and Description:**
29.3.2.2 PWM Timer’s Working Modes and Timing Event Generation
The PWM timer has three working modes, selected by the PWMx timer mode register:

- Count-Up Mode:
  In this mode, the PWM time increments from zero until reaching the value configured in the period register. Once done, the PWM timer returns to zero and starts increasing again. PWM period is equal to the value of period register + 1.

**Footer:**
Espressif Systems
653 ESP32 TRM (Version 5.6)
Submit Documentation Feedback