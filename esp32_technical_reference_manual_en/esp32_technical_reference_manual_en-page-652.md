**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack**

---

### Submodule

| **Configuration Parameter set Option Carrier frequency:** |
|---|
| - Configure duration of the first pulse in the carrier waveform. |
| - Set up the duty cycle of the following pulses. |
| | PWM Carrier |
| | Bypass the PWM carrier module. The PWM waveform will be passed through without modification. |
| | Configure if and how the PWM module should react to fault event signals. |

- Specify the action taken when a fault event occurs:
  - Force PWMXA and/or PWMXB high.
  - Force PWMXA and/or PWMXB low.

- Configure PWMXA and/or PWMXB to ignore any fault event.

### Fault Handler

- Configure how often the PWM should react to fault events:

  | **Fault Detection Submodule** |
  |---|
  | One-shot |
  | Cycle-by-cycle |
  | Generate interrupts. |

- Bypass the fault handler submodule entirely.
- Set up an option for cycle-by-cycle actions clearing.

- If desired, independently-configured actions can be taken when time-base counter is counting down or up.

---

**Subtitle:**
29.3.1.4 Fault Detection Submodule

**Figure 29.3-4. Fault Detection Submodule**

| **Configuration parameters:** |
|---|
| - Enable fault event generation and configure the polarity of fault event generation for every fault signal |
| | FAULT0 |
| | - fault event 0 |
| | FAULT1 |
| | - fault event 0 |
| | FAULT2 |
| | - fault event 0 |

---

**Footer:**
Espressif Systems
652 ESP32 TRM (Version 5.6)
Submit Documentation Feedback