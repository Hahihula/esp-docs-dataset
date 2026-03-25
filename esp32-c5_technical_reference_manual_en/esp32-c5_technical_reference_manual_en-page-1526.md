

```markdown
Chapter 41 Motor Control PWM (MCPWM)    GoBack

- A fault condition can force the PWM output to either high or low logic levels.

• Capture Module:

- Clock of the capture module is the same as MCPWM’s core clock.
- Speed measurement of rotating machinery.
- Measurement of elapsed time between position sensor pulses
- Period and duty cycle measurement of pulse train signals
- Decoding current or voltage amplitude derived from duty-cycle-encoded signals of current/voltage sensors
- Three individual capture channels, each of which with a time-stamp register (32-bit)
- Selection of edge polarity and prescaling of input capture signals
- The capture timer can sync with a PWM timer or external signals.
- Interrupt on each of the three capture channels

• ETM Module:

- Generation of different events depending on the different running states of each timer and operator.
- Each timer and operator responds to its corresponding task and automatically performs the corresponding operation.
- Each event and task can be enabled independently. When an event is not enabled, the corresponding event will not be generated. When a task is not enabled, the corresponding task will not be responded to.
```