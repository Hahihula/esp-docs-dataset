**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header: Operation and Configuration Tips**

This section provides operational tips and set-up options for the fault handler submodule.

Fault signals coming from pins are sampled and synced in the GPIO matrix. In order to guarantee successful sampling of fault pulses, each pulse duration must be at least two APB clock cycles. The fault detection submodule will then sample fault signals by using PWMyclk. So, the duration of fault pulses coming from GPIO matrix must be at least one PWMyclk cycle. Differently put, regardless of the period relation between APB clock and PWMyclk, the width of fault signal pulses on pins must be at least equal to the sum of two APB clock cycles and one PWMyclk cycle.

Each level of fault signals, FAULT0 to FAULT2, can be used by the fault handler submodule to generate fault events (fault_event0 to fault_event2). Every fault event can be configured individually to provide CBC action, OST action, or none.

**Subsection Header: Cycle-by-Cycle (CBC) action**

When CBC action is triggered, the state of PWMxA and PWMxB will be changed immediately according to the configuration of fields MCPWM_FHx_A_CBC_U/D and MCPWM_FHx_B_CBC_U/D. Different actions can be indicted when the PWM timer is incrementing or decrementing. Different CBC action interrupts can be triggered for different fault events. Status field MCPWM_FHx_CBC_ON indicates whether a CBC action is on or off. When the fault event is no longer present, CBC actions on PWMxA/B will be cleared at a specified point, which is either D/UTEP or D/UTEZ event. Field MCPWM_FHX_CBCPULSE determines at which event PWMxA and PWMxB will be able to resume normal actions. Therefore, in this mode, the CBC action is cleared or refreshed upon every PWM cycle.

**Subsection Header: One-Shot (OST) action**

When OST action is triggered, the state of PWMxA and PWMxB will be changed immediately, depending on the setting of fields MCPWM_FHx_Aca OST_U/D and MCPWM_FHx_Bca OST_U/D. Different actions can be configured when PWM timer is incrementing or decrementing. Different OST action interrupts can be triggered from different fault events. Status field MCPWM_FHXca OST_ON indicates whether an OST action on or off. The OST actions on PWMxA/B are not automatically cleared when the fault event is no longer present. One-shot actions must be cleared manually by setting the rising edge of the MCPWMca CLRca OST bit.

**Subsection Header: Capture Submodule**

**Subsubsection Header: Introduction (36.3.4.1)**

The capture submodule contains three complete capture channels. Channel inputs CAPO, CAP1 and CAP2 are sourced from the GPIO matrix. Thanks to the flexibility of the GPIO matrix, CAP0, CAP1 and CAP2 can be configured from any pin input. Multiple capture channels can be sourced from the same pin input, while prescaling for each channel can be set differently. Also, capture channels are sourced from different pins. This provides several options for handling capture signals by hardware in the background, instead of having them processed directly by the CPU. A capture submodule has the following independent key resources:

- One 32-bit timer (counter) which can be synchronized with the PWM timer, another submodule or software.
- Three capture channels, each equipped with a 32-bit time-stamp and a capture prescaler.
- Independent edge polarity (rising/falling edge) selection for any capture channel.

**Footer:**
Espressif Systems
1359 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback