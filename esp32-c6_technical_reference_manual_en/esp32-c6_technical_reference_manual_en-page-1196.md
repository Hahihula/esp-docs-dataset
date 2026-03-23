

```markdown
| Submodule                  | Configuration Parameter or Option and time relationship between upper and lower switches. |
|----------------------------|-------------------------------------------------------------------------------------------------------------|
| Dead Time Generator        | • Specify the dead time on rising edge.<br>• Specify the dead time on falling edge.<br>• Bypass the dead time generator module. The PWM waveform will pass through without inserting dead time.<br>• Allow PWMxB phase shifting with respect to the PWMxA output.<br>Configure updating method for this submodule.<br>Enable carrier and set up carrier frequency. |
| PWM Carrier                | • Configure duration of the first pulse in the carrier waveform.<br>• Configure the duty cycle of the following pulses.<br>• Bypass the PWM carrier module. The PWM waveform will be passed through without modification.<br>Configure if and how the PWM module should react the fault event signals.<br>Specify the action taken when a fault event occurs:<ul><li>Force PWMxA and/or PWMB high.</li><li>Force PWMxA and/or PWMB low.</li><li>Configure PWMxA and/or PWMB to ignore any fault event.</li></ul> |
| Fault Handler              | • Configure how often the PWM should react to fault events:<ul><li>One-shot</li><li>Cycle-by-cycle</li></ul><br>• Generate interrupts.<br>• Bypass the fault handler submodule entirely.<br>• Configure an option for cycle-by-cycle actions clearing.<br>• If desired, independently-configured actions can be taken when time-base counter is counting down or up. |
```

### 36.3.1.4 Fault Detection Module

![Figure 36.3-4. Fault Detection Module](#)

```text
FAULT0 → FAULT DETECT → fault event 0
FAULT1 →                     → fault event 0
FAULT2 →                     → fault event 0
```

Configuration options:

* Enable fault event generation and configure the polarity of fault event generated for every fault signal.
* Generate fault event interrupts.
```