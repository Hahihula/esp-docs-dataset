

```markdown
Figure 56.2-1. MCPWM Module Overview

Below is an overview of the submodules' functionality in Figure 56.2-1:

*   PWM Timers 0, 1, and 2:
    -   Every PWM timer has a dedicated 8-bit clock prescaler.
    -   The 16-bit counter in the PWM timer can work in Count-Up Mode, Count-Down Mode, or Count-Up-Down Mode.
    -   A hardware sync or software sync can trigger a reload on the PWM timer with a phase register. It will also trigger the prescaler's restart, so that the timer's clock can also be synced. The source of the hard sync can come from any GPIO or any other PWM timer's sync_out. The source of the soft sync comes from writing toggle value to the MCPWM_TIMERn_SYNC_SW bit.

*   PWM Operators 0, 1, and 2:
    -   Every PWM operator has two PWM outputs: PWMxA and PWMxB. They can work independently, in symmetric or asymmetric configurations.
    -   The control of the PWM signal can be updated asynchronously.
    -   Configurable dead time on rising and falling edges; each set up independently.
    -   All events can trigger CPU interrupts.
    -   Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer.
    -   Period, time stamps, and important control registers have shadow registers with flexible updating methods.

*   Fault Detection Module:
    -   Programmable fault handling in both cycle-by-cycle mode and one-shot mode.
```