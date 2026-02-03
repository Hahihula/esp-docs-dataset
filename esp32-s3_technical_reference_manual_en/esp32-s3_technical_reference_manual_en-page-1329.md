**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Number and Name:**
36.3 Submodules

**Subsection Header:**
36.3.1 Overview

**Body Text:**
This section lists the configuration parameters of key submodules. For information on adjusting a specific parameter, e.g., synchronization source of PWM timer, please refer to Section 36.3.2 for details.

**Sub-subsection Number and Name with Figure Reference (with figure):**
36.3.1.1 Prescaler Submodule
- **Figure Caption:**
  - Figure 36.3-1. Prescaler Submodule

**Configuration Option Description List under "Prescaler Submodule":**
- Scale the CRYPTO_PWM_CLK.

**Sub-subsection Number and Name with Figure Reference (with figure):**
36.3.1.2 Timer Submodule
- **Figure Caption:**
  - Figure 36.3-2. Timer Submodule

**Configuration Options Description List under "Timer Submodule":**
- Set the PWM timer frequency or period.
- Configure the working mode for the timer:
  - Count-Up Mode: for asymmetric PWM outputs
  - Count-Down Mode: for asymmetric PWM outputs
  - Count-Up-Down Mode: for symmetric PWM outputs

**Additional Configuration Options Description List under "Timer Submodule":**
- Configure the reloading phase (including the value and the direction) used during software and hardware synchronization.
- Synchronize the PWM timers with each other. Either hardware or software synchronization may be used.

**Final Configuration Option Description:**
- Configure the source of the PWM timer’s the synchronization input to one of the seven sources below:

**Footer Information:**
Espressif Systems
1329

**Document Reference and Feedback Link (with link text):**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback