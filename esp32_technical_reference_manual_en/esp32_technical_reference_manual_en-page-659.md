**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** [GoBack](#)

**Section Heading:**
The PWM generator submodule performs the following actions:

- **Bullet Points List of Actions:**
  - Generation of timing events based on time stamps configured using the A and B registers. Events happen when the following conditions are satisfied:
    - UTEA: the PWM timer is counting up and its value is equal to register A.
    - UTEB: the PWM timer is counting down and its value is equal to register B.
  - DTEA: the PWM timer is counting down and its value is equal to register A.
  - DTEB: the PWM timer is counting down and its value is equal to register B.

- **Additional Actions Listed Below:**
  - Generation of U/DT1, U/DT2 timing events based on fault or synchronization events.
  - Management of priority when these timing events occur concurrently.
  - Qualification and generation of set, clear and toggle actions, based on the timing events.
  - Controlling of the PWM duty cycle, depending on configuration of the PWM generator submodule.
  - Handling of new time stamp values, using shadow, registers to prevent glitches in the PWM cycle.

**Subsection Heading:**
PWM Operator Shadow Registers

- **Paragraph Description:** The time stamp registers A and B, as well as action configuration registers PWM_GENx_A_REG and PWM_GENx_B_REG are shadowed. Shadowing provides a way of updating registers in sync with the hardware. For a description of the shadow registers, please see 29.3.2.3.

**Subsection Heading:**
Timing Events

- **Paragraph Description:** For convenience, all timing signals and events are summarized in Table 29.3-2.

**Table Title:**
Table 29.3-2. Timing Events Used in PWM Generator

| Signal | Event Description | PWM Timer Operation |
|--------|-------------------|----------------------|
| DTEP   | PWM timer value is equal to the period register value | PWM timer counts down. |
| DTEZ   | PWM timer value is equal to zero |  |
| DTEA   | PWM timer value is equal to A register |  |
| DTEB   | PWM timer value is equal to B register |  |
| DTO event | Based on fault or synchronization events |  |
| DT1 event | Based on fault or synchronization events |  |
| UTEP   | PWM timer value is equal to the period register value | PWM timer counts up. |
| UTEZ   | PWM timer value is equal to zero |  |
| UTEA   | PWM timer value is equal to A register |  |
| UTEB   | PWM timer value is equal to B register |  |
| UTO event | Based on fault or synchronization events |  |
| UT1 event | Based on fault or synchronization events |  |
| Software-force event | Software-initiated asynchronous event | N/A |

- **Paragraph Description:** The purpose of a software-force event is to impose non-continuous or continuous changes on the PWMxA and PWMxB outputs. The change is done asynchronously. Software-force control is handled by the PWM_PWM_GENx FORCE_REG registers.

**Footer:**
Espressif Systems  
659  
ESP32 TRM (Version 5.6)  

**Link:** Submit Documentation Feedback