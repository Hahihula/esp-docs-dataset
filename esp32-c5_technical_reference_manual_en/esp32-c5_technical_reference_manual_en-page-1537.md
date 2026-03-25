

```markdown
- DTO: the PWM timer is counting down and FAULT0 detected (field MCPWM_GENn_TO_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_TO_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_TO_SEL is set to 2) or synchronized (field MCPWM_GENn_TO_SEL is set to 3).
- DT1: the PWM timer is counting down and FAULT0 detected (field MCPWM_GENn_T1_SEL is set to 0) or FAULT1 detected (field MCPWM_GENn_T1_SEL is set to 1) or FAULT2 detected (field MCPWM_GENn_T1_SEL is set to 2) or synchronized (field MCPWM_GENn_T1_SEL is set to 3).

- Management of priority when these timing events occur concurrently.
- Generation of set, clear, and toggle actions, based on the timing events.
- Controlling of the PWM duty cycle, depending on the configuration of the PWM generator module.
- Handling of new time stamp values, using shadow registers to prevent glitches in the PWM cycle.

Shadow Register of PWM Generator

The time stamp registers A and B used by the hardware have shadow registers, which are registers MCPWM_GENn_A_REG and MCPWM_GENn_B_REG. Shadowing provides a way of updating registers in sync with the hardware.

When MCPWM_GLOBAL_UP_EN is set to 1, the shadow registers can be written to the active register at a specified time. The update method field for MCPWM_GENn_A_REG and MCPWM_GENn_B_REG is MCPWM_GENn_CFG_UPMETHOD. Software can also trigger a globally forced update bit MCPWM_GLOBAL_FORCE_UP which will prompt all registers in the module to be updated according to shadow registers. For a description of the shadow registers, please see Section 41.3.2.3.

Timing Events

For convenience, all timing signals and events are summarized in Table 41.3-2.

Table 41.3-2. Timing Events Used in PWM Generator

| Signal       | Event Description                                                                 | PWM Timer Operation |
|--------------|------------------------------------------------------------------------------------|---------------------|
| DTEP         | PWM timer value is equal to the period register value                              |                     |
| DTEZ         | PWM timer value is equal to zero                                                  |                     |
| DTEA         | PWM timer value is equal to register A                                            |                     |
| DTEB         | PWM timer value is equal to register B                                            | PWM timer counts down |
| DTO event    | Based on fault or synchronization events                                          |                     |
| DT1 event    | Based on fault or synchronization events                                          |                     |
| UTEP         | PWM timer value is equal to the period register value                             |                     |
| UTEZ         | PWM timer value is equal to zero                                                  |                     |
| UTEA         | PWM timer value is equal to register A                                            | PWM timer counts up  |
| UTB          | PWM timer value is equal to register B                                            |                     |
| UTO event     | Based on fault or synchronization events                                          |                     |
| UT1 event     | Based on fault or synchronization events                                          |                     |
| Software-force event | Software-initiated asynchronous event                                       | N/A                 |

The purpose of a software-force event is to impose non-continuous or continuous changes on the PWMxA and PWMxB outputs. The change is done asynchronously. Software-force control is handled by the
```