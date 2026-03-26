
```markdown
Chapter 56 Motor Control PWM (MCPWM)

GoBack

56.3.3.1 PWM Generator Module

Purpose of the PWM Generator Module

In this module, important timing events are generated or imported. The events are then converted into specific actions to generate the desired waveforms at the PWMxA and PWMxB outputs.

The PWM generator module performs the following actions:

* Generation of timing events based on time stamps configured using the A and B registers. Events happen when the following conditions are met (for the configuration of registers A and B, see section 56.3.3.1):

    - UTEA: the PWM timer is counting up and its value is equal to register A.
    - UTB: the PWM timer is counting up and its value is equal to register B.
    - DTEA: the PWM timer is counting down and its value is equal to register A.
    - DTB: the PWM timer is counting down and its value is equal to register B.

* Generation of U/DTO, U/DT1 timing events based on fault or synchronization events.

    - UTO: the PWM timer is counting up and FAULT0 detected (field MCPWM_GENn_TO_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_TO_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_TO_SEL is set to 2) or synchronized (field MCPWM_GENn_TO_SEL is set to 3).

    - UT1: the PWM timer is counting up and FAULT0 detected (field MCPWM_GENn_T1_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_T1_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_T1_SEL is set to 2) or synchronized (field MCPWM_GENn_T1_SEL is set to 3).

    - DTO: the PWM timer is counting down and FAULT0 detected (field MCPWM_GENn_TO_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_TO_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_TO_SEL is set to 2) or synchronized (field MCPWM_GENn_TO_SEL is set to 3).

    - DT1: the PWM timer is counting down and FAULT0 detected (field MCPWM_GENn_T1_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_T1_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_T1_SEL is set to 2) or synchronized (field MCPWM_GENn_T1_SEL is set to 3).

* Management of priority when these timing events occur concurrently.
* Generation of set, clear, and toggle actions, based on the timing events.
* Controlling of the PWM duty cycle, depending on the configuration of the PWM generator module.
* Handling of new time stamp values, using shadow registers to prevent glitches in the PWM cycle.

Shadow Register of PWM Generator

The time stamp registers A and B used by the hardware have shadow registers, which are registers MCPWM_GENn_A_REG and MCPWM_GENn_B_REG. Shadowing provides a way of updating registers in sync with the hardware.

When MCPWM_GLOBAL_UP_EN is set to 1, the shadow registers can be written to the active register at a specified time. The update method field for MCPWM_GENn_A_REG and MCPWM_GENn_B_REG is MCPWM_GENn_CFG_UPMETHOD. Software can also trigger a globally forced update bit
```