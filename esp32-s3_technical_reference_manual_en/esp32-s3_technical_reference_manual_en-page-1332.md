**Chapter Title:**
Motor Control PWM (MCPWM)

**Figure Caption and Description:**
- **Figure 36.3-4:** Fault Detection Submodule

**Body Text with List Item:**
- Generate fault event interrupts

**Subsection Heading:**
36.3.1.5 Capture Submodule

**Figure Caption for Figure 36.3-5:**
Capture Submodule
- CAP0, CAP1, CAP2 are connected to the capture module.

**Body Text with List Item:**
Configuration options:
- Select the edge polarity and prescaling of the capture input.
- Set up a software-triggered capture.
- Configure the capture timer’s sync trigger and sync phase.
- Software syncs the capture timer.

**Subsection Heading:**
36.3.2 PWM Timer Submodule

**Body Text with List Item:**
Each MCPWM module has three PWM timer submodules. Any of them can determine the necessary event timing for any of the three PWM operator submodules. Built-in synchronization logic allows multiple PWM timer submodules, in one or more MCPWM modules, to work together as a system, when using synchronization signals from the GPIO matrix.

**Subsection Heading:**
36.3.2.1 Configurations of the PWM Timer Submodule

**Body Text with List Item:**
Users can configure the following functions of the PWM timer submodule:
- Control how often events occur by specifying the PWM timer frequency or period.
- Configure a particular PWM timer to synchronize with other PWM timers or modules.
- Get a PWM timer in phase with other PWM timers or modules.

- Set one of the following timer counting modes: count-up, count-down, count-up-down. 

**Footer Information:**
Espressif Systems
1332 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback