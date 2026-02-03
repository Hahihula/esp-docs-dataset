**Chapter Title:**
Motor Control PWM (MCPWM)

**GoBack Link:** [GoBack](#)

---

**Table Title:**
Table 36.3-1. Configuration Parameters of the Operator Submodule

| Submodule                   | Configuration Parameter or Option for PWMxA and/or PWMxB output |
|------------------------------|------------------------------------------------------------------|
| **PWM Generator**            | - Set up at which time the timing events occur.<br>- Define what action should be taken on timing events:<br>  - Switch high or low of PWMxA and/or PWMxB outputs<br>  - Toggle PWMxA and/or PWMxB outputs<br>  - Take no action on outputs |
|                              | - Use direct s/w control to force the state of PWM outputs |
|                              | - Add a dead time to raising edge and/or failing edge on PWM outputs. |
|                              | - Configure update method for this submodule.<br>- Control complementary dead time relationship between upper and lower switches. |
| **Dead Time Generator**      | - Specify the dead time on rising edge.<br>- Specify the dead time on falling edge.<br>- Bypass the dead time generator module. The PWM waveform will pass through without inserting dead time. |
|                              | - Allow PWMxB phase shifting with respect to the PWMxA output. |
|                              | - Configure updating method for this submodule.<br>Enable carrier and set up carrier frequency. |
| **PWM Carrier**              | - Configure duration of the first pulse in the carrier waveform.<br>- Set up the duty cycle of the following pulses.<br>- Bypass the PWM carrier module. The PWM waveform will be passed through without modification.<br>Configure if and how the PWM module should react to fault event signals. |
|                              | - Specify the action taken when a fault event occurs:<br>  - Force PWMxA and/or PWMxB high.<br>  - Force PWMxA and/or PWMxB low.<br>  - Configure PWMxA and/or PWMxB to ignore any fault event. |
| **Fault Handler**            | - Configure how often the PWM should react to fault events:<br>  - One-shot<br>  - Cycle-by-cycle |
|                              | - Generate interrupts.<br>- Bypass the fault handler submodule entirely.<br>- Set up an option for cycle-by-cycle actions clearing. |
|                              | - If desired, independently-configured actions can be taken when time-base counter is counting down or up. |

---

**Subsection Title:**
36.3.1.4 Fault Detection Submodule

**Configuration Options:**  
- Enable fault event generation and configure the polarity of fault event generation for every fault signal.

**Footer Information:**
Espressif Systems  
Page 1331 ESP32-S3 TRM (Version 1.7)  

**Feedback Link:** [Submit Documentation Feedback](#)