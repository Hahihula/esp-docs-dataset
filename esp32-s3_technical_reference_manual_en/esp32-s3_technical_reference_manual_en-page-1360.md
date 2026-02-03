**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**

- Input capture signal prescaling (from 1 to 256).
- Interrupt capabilities on any of the three capture events.

**Subtitle and Section Number:** 
36.3.4.2 Capture Timer

**Body Text for Subsection "Capture Timer":**
The capture timer is a 32-bit counter incrementing continuously. It is enabled by setting MCPWM_CAP_TIMER_EN to 1. Its operating clock source is APB_CLK. When MCPWM_CAP_SYNCI_EN is configured, the counter will be loaded with phase stored in register MCPWM_CAP_TIMER_PHASE_REG at the time of a sync event. Sync events can select from PWM timers sync-out, PWM module sync-in by configuring MCPWM_CAP_SYNCI_SEL. Sync event can also generate by setting MCPWM_CAP_SYNC_SW. The capture timer provides timing references for all three capture channels.

**Subtitle and Section Number:** 
36.3.4.3 Capture Channel

**Body Text for Subsection "Capture Channel":**
The capture signal coming to a capture channel will be inverted first, if needed, and then prescaled. Each capture channel has a prescaler register of MCPWM_CAPx_PRESCALE. Finally, specified edges of preprocessed capture signal will trigger capture events. Setting MCPWM_CAPx_EN to enable a capture channel. The capture event occurs at the time selected by the MCPWM_CAPx_MODE. When a capture event occurs, the capture timer’s value is stored in timestamp register MCPWM_CAP_CHx_REG. Different interrupts can be generated for different capture channels at capture events. The edge that triggers a capture event is recorded in register MCPWM_CAPx_EDGE. The capture event can be also forced by software setting MCPWM_CAPx_SW.

**Footer:**
Espressif Systems
1360 ESP32-S3 TRM (Version 1.7)