

```markdown
Figure 41.3-28. Possible Duty Cycle Settings for Sustaining Pulses in the PWM Carrier Submodule

41.3.3.4 Fault Detection Module

Each MCPWM peripheral is connected to three fault signals (FAULT0, FAULT1, and FAULT2) which are sourced from the GPIO matrix. These signals are intended to indicate external fault conditions, and may be preprocessed by the Fault Detection module to generate fault events. Fault events can then execute the user code to control MCPWM outputs in response to specific faults.

Function of Fault Detection Module

The key actions performed by the fault detection module are:

- Forcing outputs PWMxA and PWMxB, upon detected fault, to one of the following states:
  - High
  - Low
  - Toggle
  - No action taken

- Execution of one-shot trip (OST) upon detection of over-current conditions/short circuits.

- Cycle-by-cycle trip (CBC) to provide current-limiting operation.

- Allocation of either one-shot or cycle-by-cycle operation for each fault signal.

- Generation of interrupts for each fault input.

- Support for software-force tripping.

- Enabling or disabling of module function as required.
```