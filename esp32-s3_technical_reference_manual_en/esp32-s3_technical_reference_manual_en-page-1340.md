**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Header:**
36.3.3.1 PWM Generator Submodule

**Subsection Title:**
Purpose of the PWM Generator Submodule

**Body Text:**
In this submodule, important timing events are generated or imported. The events are then converted into specific actions to generate the desired waveforms at the PWMx A and PWMx B outputs.

The PWM generator submodule performs the following actions:
- Generation of timing events based on time stamps configured using the A and B registers. Events happen when the following conditions are satisfied:
  - UTEA: the PWM timer is counting up and its value is equal to register A.
  - UTEB: the PWM timer is counting up and its value is equal to register B.
  - DTEA: the PWM timer is counting down and its value is equal to register A.
  - DTEB: the PWM timer is counting down and its value is equal to register B.

- Generation of U/DT1, U/DT2 timing events based on fault or synchronization events.

- Management of priority when these timing events occur concurrently.

- Qualification and generation of set, clear and toggle actions, based on the timing events.
  
- Controlling of the PWM duty cycle, depending on configuration of the PWM generator submodule.

- Handling of new time stamp values, using shadow registers to prevent glitches in the PWM cycle.

**Subsection Title:**
PWM Operator Shadow Registers

**Body Text:**
The time stamp registers A and B, as well as action configuration registers MCPWM_GENx_A_REG and MCPWM_GENx_B_REG are shadowed. Shadowing provides a way of updating registers in sync with the hardware.
When MCPWM_GLOBAL_UP_EN is set to 1, the shadow registers can be written to the active register at a specified time. The update method fields for time stamp registers A and B are MCPWM_GEN_A_UPMETHOD and MCPWM_GEN_B_UPMETHD. The update method field for MCPWM_GENx_A_REG and MCPWM_GENx_B_REG is MCPWM_GEN_CFG_UPMETHD. Software can also trigger a globally forced update bit MCPWM_GLOBALFORCE_UP which will prompt all registers in the module to be updated according to shadow registers.

**Subsection Title:**
Timing Events

**Body Text:**
For convenience, all timing signals and events are summarized in Table 36.3-2.
  
**Table Header (Title):**
Table 36.3-2. Timing Events Used in PWM Generator

| Signal | Event Description | PWM Timer Operation |
|--------|-------------------|----------------------|
| DTEP   | PWM timer value is equal to the period register value |                 |
| DTEZ   | PWM timer value is equal to zero                   |                 |
| DTEA   | PWM timer value is equal to A register              | PWM timer counts down. |
| DTEB   | PWM timer value is equal to B register             |                 |

**Footer:**
Espressif Systems
1340 ESP32-S3 TRM (Version 1.7)