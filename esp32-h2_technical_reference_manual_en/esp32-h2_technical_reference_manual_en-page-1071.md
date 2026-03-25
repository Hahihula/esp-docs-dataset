

```markdown
## 36.3.3.1 PWM Generator Module

### Purpose of the PWM Generator Module

In this module, important timing events are generated or imported. The events are then converted into specific actions to generate the desired waveforms at the `PWMxA` and `PWMxB` outputs.

The PWM generator module performs the following actions:

*   Generation of timing events based on time stamps configured using the A and B registers. Events happen when the following conditions are met:
    *   UTEA: the PWM timer is counting up and its value is equal to register A.
    *   UTEB: the PWM timer is counting up and its value is equal to register B.
    *   DTEA: the PWM timer is counting down and its value is equal to register A.
    *   DTBE: the PWM timer is counting down and its value is equal to register B.

*   Generation of U/DTO, U/DT1 timing events based on fault or synchronization events.
    *   UTO: the PWM timer is counting up and FAULT0 detected (field `MCPWM_GENx_TO_SEL` is set to 0) or FAULT1 detected (field `MCPWM_GENx_TO_SEL` is set to 1) or FAULT2 detected (field `MCPWM_GENx_TO_SEL` is set to 2) or synchronized (field `MCPWM_GENx_TO_SEL` is set to 3).
    *   UT1: the PWM timer is counting up and FAULT0 detected (field `MCPWM_GENx_T1_SEL` is set to 0) or FAULT1 detected (field `MCPWM_GENx_T1_SEL` is set to 1) or FAULT2 detected (field `MCPWM_GENx_T1_SEL` is set to 2) or synchronized (field `MCPWM_GENx_T1_SEL` is set to 3).
    *   DTO: the PWM timer is counting down and FAULT0 detected (field `MCPWM_GENx_TO_SEL` is set to 0) or FAULT1 detected (field `MCPWM_GENx_TO_SEL` is set to 1) or FAULT2 detected (field `MCPWM_GENx_TO_SEL` is set to 2) or synchronized (field `MCPWM_GENx_TO_SEL` is set to 3).
    *   DT1: the PWM timer is counting down and FAULT0 detected (field `MCPWM_GENx_T1_SEL` is set to 0) or FAULT1 detected (field `MCPWM_GENx_T1_SEL` is set to 1) or FAULT2 detected (field `MCPWM_GENx_T1_SEL` is set to 2) or synchronized (field `MCPWM_GENx_T1_SEL` is set to 3).

*   Management of priority when these timing events occur concurrently
*   Generation of set, clear, and toggle actions, based on the timing events
*   Controlling of the PWM duty cycle, depending on the configuration of the PWM generator module
*   Handling of new time stamp values, using shadow registers to prevent glitches in the PWM waveform

### Shadow Register of PWM Operator

The time stamp registers A and B, as well as action configuration registers `MCPWM_GENx_A_REG` and `MCPWM_GENx_B_REG` are shadowed. Shadowing provides a way of updating registers in sync with the hardware.

When `MCPWM_GLOBAL_UP_EN` is set to 1, the shadow registers can be written to the active register at a specified time. The update method field for `MCPWM_GENx_A_REG` and `MCPWM_GENx_B_REG` is `MCPWM_GENx_CFG_UPMETHOD`. The software can also trigger a globally forced update bit `MCPWM_GLOBAL_FORCE_UP` which will prompt all registers in the module to be updated according to shadow registers. For a description of the shadow registers, please see Section 36.3.2.3.
```