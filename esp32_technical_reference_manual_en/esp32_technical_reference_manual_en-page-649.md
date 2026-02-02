**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Body Text:**

- Programmable fault handling allocated on fault condition in both cycle-by-cycle mode and one-shot mode.
- A fault condition can force the PWM output to either high or low logic levels.

**Subtitle: Capture Module**

- Speed measurement of rotating machinery
- Measurement of elapsed time between position sensor pulses
- Period and duty-cycle measurement of pulse train signals
- Decoding current or voltage amplitude derived from duty-cycle-encoded signals from current/voltage sensors
- Three individual capture channels, each of which has a time-stamp register (32 bits)
- Selection of edge polarity and prescaling of input capture signal

- The capture timer can sync with a PWM timer or external signals.
- Interrupt on each of the three capture channels

**Section 29.3 Submodules**

**Subsection: Overview**
This section lists the configuration parameters of key submodules. For information on adjusting a specific parameter, e.g., synchronization source of PWM timer, please refer to Section 29.3.2 for details.

**Subsection Title:** 
29.3.1 Overview

**Sub-subsection title and content:**
29.3.1.1 Prescaler Submodule
- Configuration parameter:
  - Scale the PWM clock according to CLK_160M.
  
**Diagram Description (Figure Caption):**
Figure 29.3-1. Prescaler Submodule
  
**Diagram Content:** 
A block diagram showing the connection between CLK_160M, CLOCK PRESICALER, and PWM_CLK.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)