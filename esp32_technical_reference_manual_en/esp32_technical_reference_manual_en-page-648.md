**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description:**
Figure 29.2-1 shows a block diagram of the MCPWM module, including components such as:
- TIMERS labeled as TIMER 0 and TIMER 1.
- A CLOCK PRESCALER component connected to CLK_160M.
- A section for GPIO MATRIX with labels like PWM0A through PWM2B.

**Subtitle:**
Figure 29.2-1. MCPWM Module Overview

**Body Text:**

An overview of the submodules’ function in Figure 29.2-1 is shown below:

- **PWM Timers O, and 2**
  - Every PWM timer has a dedicated 8-bit clock prescaler.
  - The 16-bit counter in the PWM timer can work in count-up mode or count-down down mode.

- A hardware sync can trigger a reload on the PWM timer with a phase register. It will also trigger the prescaler restart, so that the timer’s clock can be also synced. The source of the sync can come from any GPIO or any other PWM timer's sync_out.
  
- **PWM Operators 0, and 2**
  - Every PWM operator has two PWM outputs: PWMx_A and PWMx_B. They can work independently in symmetric and asymmetric configuration.

- Software, asynchronous override control of PWM signals
- Configurable dead-time on rising and falling edges; each set up independently.
- All events can trigger CPU interrupts.
- Modulating of PWM output by high-frequency carrier signals, useful when gate drives are insulated with a transformer.
- Period, time stamps and important control registers have shadow registers with flexible updating methods.

**List:**
- Fault Detection Module

**Footer Information:**
Espressif Systems
648 ESP32 TRM (Version 5.6)
Submit Documentation Feedback