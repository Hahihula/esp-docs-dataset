**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**
All seven settings of the duty cycle are shown in Figure 36.3-28.

**Figure Caption and Description:**
Figure 36.3-28 shows Possible Duty Cycle Settings for Sustaining Pulses in the PWM Carrier Submodule.
The figure includes a diagram with multiple horizontal lines labeled as "Duty" followed by fractions (1/8, 2/8, etc.), indicating different duty cycle settings.

**Subsection Title:**
36.3.3.4 Fault Handler Submodule

**Body Text under Subsection:**
Each MCPWM peripheral is connected to three fault signals (FAULT0, FAULT1 and FAULT2) which are sourced from the GPIO matrix. These signals are intended to indicate external fault conditions, and may be preprocessed by the fault detection submodule to generate fault events. Fault events can then execute the user code to control MCPWM outputs in response to specific faults.

**Subsection Title:**
Function of Fault Handler Submodule

**Body Text under Subsection:**
The key actions performed by the fault handler submodule are:
- Forcing outputs PWMxA and PWMxB, upon detected fault, to one of the following states:
  - High
  - Low
  - Toggle
  - No action taken
- Execution of one-shot trip (OST) upon detection of over-current conditions/short circuits.
- Cycle-by-cycle tripping (CBC) to provide current-limiting operation.
- Allocation of either one-shot or cycle-by-cycle operation for each fault signal.
- Generation of interrupts for each fault input.
- Support for software-force tripping.
- Enabling or disabling of submodule function as required.

**Footer:**
Espressif Systems
1358 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback