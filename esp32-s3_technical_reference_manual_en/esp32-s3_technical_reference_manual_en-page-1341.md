**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Table of Signals, Event Descriptions and PWM Timer Operation**

| Signal       | Event Description                                    | PWM Timer Operation                          |
|-------------|-------------------------------------------------------|-----------------------------------------------|
| DTO event   | Based on fault or synchronization events              |                                                |
| DT1 event   | Based on fault or synchronization events              |                                                |
| UTEP        | PWM timer value is equal to the period register value |                                                |
| UTEZ        | PWM timer value is equal to zero                      |                                                |
| UTEA        | PWM timer value is equal to A register                | PWM timer counts up.                          |
| UTEB        | PWM timer value is equal to B register               |                                                |
| UTO event   | Based on fault or synchronization events              |                                                |
| UT1 event   | Based on fault or synchronization events              |                                                |
| Software-force event | Software-initiated asynchronous event  | N/A                                           |

**Body Text:**
The purpose of a software-force event is to impose non-continuous or continuous changes on the PWMXA and PWMXB outputs. The change is done asynchronously. Software-force control is handled by the MCPWM_GENX_FORCE_REG registers.

The selection and configuration of TO/T1 in the PWM generator submodule is independent of the configuration of fault events in the fault handler submodule. A particular trip event may or may not be configured to cause trip action in the fault handler submodule, but the same event can be used by the PWM generator to trigger T0/T1 for controlling PWM waveforms.

It is important to know that when the PWM timer is in count-up-down mode, it will always decrement after a TEP event and will always increment after a TEZ event. So when the PWM timer is in count-up-down mode, DTEP and UTEZ events will occur while the events UTEP and DTEZ will never occur.

The PWM generator can handle multiple events at the same time. Events are prioritized by the hardware and relevant details are provided in Table 36.3-3 and Table 36.3-4. Priority levels range from 1 (the highest) to 7 (the lowest). Please note that the priority of TEP and TEZ events depends on the PWM timer’s direction.

If the value of A or B is set to be greater than the period, then U/DTEA and U/DTEB will never occur.

**Table Title:**
Table 36.3-3. Timing Events Priority When PWM Timer Increments

| Priority Level | Event |
|----------------|-------|
| 1 (highest)    | Software-force event |
| 2              | UTEP   |
| 3              | UTO    |
| 4              | UT1    |
| 5              | UTEB   |
| 6              | UTEA   |
| 7 (lowest)     | UTEZ   |

**Table Title:**
Table 36.3-4. Timing Events Priority when PWM Timer Decrements

| Priority level | Event |
|----------------|-------|
| 1 (highest)    | Software-force event |
| 2              | DTEZ   |
| 3              | DTO    |

**Footer Information:**
Espressif Systems
Page number: 1341
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback