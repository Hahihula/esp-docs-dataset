

```markdown
- Each signal out of the PWM signal pair includes a specific pattern of dead time (i.e., adding delays to the rising and falling edges of the PWM signal).
- Superimposes a carrier on the PWM signal, if configured to do so.
- Handles response under fault conditions.

Figure 41.3-12 shows the block diagram of a PWM operator.

![Block Diagram of a PWM Operator](image)

Figure 41.3-12. Block Diagram of A PWM Operator

41.3.3.1 PWM Generator Module

Purpose of the PWM Generator Module

In this module, important timing events are generated or imported. The events are then converted into specific actions to generate the desired waveforms at the PWMxA and PWMxB outputs.

The PWM generator module performs the following actions:

- Generation of timing events based on time stamps configured using the A and B registers. Events happen when the following conditions are met (for the configuration of registers A and B, see section 41.3.3.1):

    - UTEA: the PWM timer is counting up and its value is equal to register A.
    - UTEB: the PWM timer is counting up and its value is equal to register B.
    - DTEA: the PWM timer is counting down and its value is equal to register A.
    - DTEB: the PWM timer is counting down and its value is equal to register B.

- Generation of U/DTO, U/DT1 timing events based on fault or synchronization events.

    - UTO: the PWM timer is counting up and FAULT0 detected (field MCPWM_GENn_TO_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_TO_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_TO_SEL is set to 2) or synchronized (field MCPWM_GENn_TO_SEL is set to 3).
    - UT1: the PWM timer is counting up and FAULT0 detected (field MCPWM_GENn_T1_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_T1_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_T1_SEL is set to 2) or synchronized (field MCPWM_GENn_T1_SEL is set to 3).
```