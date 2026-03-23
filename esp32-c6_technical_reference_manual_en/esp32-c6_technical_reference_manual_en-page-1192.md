

```markdown
Figure 36.2-1. MCPWM Module Overview

- PWM Operators 0, 1, and 2:
  - Every PWM operator has two PWM outputs: `PWMxA` and `PWMxB`. They can work independently, in symmetric or asymmetric configurations.
  - The control of the PWM signal can be updated asynchronously.
  - Configurable dead time on rising and falling edges; each set up independently.
  - All events can trigger CPU interrupts.
  - Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer.
  - Period, time stamps, and important control registers have shadow registers with flexible updating methods.

- Fault Detection Module:
  - Programmable fault handling in both cycle-by-cycle mode and one-shot mode.
  - A fault condition can force the PWM output to either high or low logic levels.

- Capture Module:
  - Clock of the capture module is the same as MCPWM’s core clock.
  - Speed measurement of rotating machinery.
  - Measurement of elapsed time between position sensor pulses
  - Period and duty cycle measurement of pulse train signals
  - Decoding current or voltage amplitude derived from duty-cycle-encoded signals of current/voltage sensors
  - Three individual capture channels, each of which with a time-stamp register (32-bit)
```