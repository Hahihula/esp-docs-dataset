**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Subtitle:**
29.3.1.2 Timer Submodule

**Diagram Description and Labels in Image:**
- The diagram is labeled "Figure 29.3-2. Timer Submodule".
- It shows a block with inputs labeled as `PWM_TIMERx_SYNCSEL`, `timer 0 synco`, `timer 1 synco`, `timer 2 synco`, `SYNC0`, `SYNC1`, and `SYNC2`.
- The outputs are connected to `sync x in` which then connects into the `TIMERx` block.
- From `TIMERx`, there is an output labeled as `timer x status` leading out of the diagram.

**Configuration Parameters:**
- Set the PWM timer frequency or period
- Configure the working mode for the timer:
  - Count-Up Mode: for asymmetric PWM outputs
  - Count-Down Mode: for asymmetric PWM outputs
  - Count-Up-Down Mode: for symmetric PWM outputs
- Configure the reloading phase (including the value and the phase) used during software and hardware synchronization.
- Synchronize the PWM timers with each other. Either hardware or software synchronization may be used.

**Synchronization Input Sources of the PWM Timer's Synchronization Inputs:**
- The three PWM timer’s synchronization inputs:
  - Three synchronization signals from the GPIO matrix: `SYNC0`, `SYNC1`, `SYNC2`.
  - No synchronization input signal selected

**Synchronization Output Sources for the PWM Timer:**
- Configure the source of the PWM timer’s synchronization output to one of the four sources below:
  - Synchronization input signal
  - Event generated when value of the PWM timer is equal to zero
  - Event generated when value of the PWM timer is equal to period
  - No synchronization output generated

**Method for Period Updating:**
- Configure the method of period updating.

**Footer Information:**
Espressif Systems  
650 Submit Documentation Feedback ESP32 TRM (Version 5.6)