**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description:**
- Figure labeled "Figure 29.3-28" shows possible duty cycle settings for sustaining pulses in the PWM carrier submodule.
- The diagram includes a bar chart with labels such as Duty 1/8, Duty 2/8, etc., and an arrow indicating 'carrier period'.

**Subtitle:**
29.3.3.4 Fault Handler Submodule

**Body Text:**
Each MCPWM peripheral is connected to three fault signals (FAULT0, FAULT1 and FAULT2) which are sourced from the GPIO matrix. These signals are intended to indicate external fault conditions, and may be preprocessed by the fault detection submodule to generate fault events. Fault events can then execute the user code to control MCPWM outputs in response to specific faults.

**Subheading:**
Function of Fault Handler Submodule

**List Description under Function of Fault Handler Submodule:**
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
675 ESP32 TRM (Version 5.6)
Submit Documentation Feedback