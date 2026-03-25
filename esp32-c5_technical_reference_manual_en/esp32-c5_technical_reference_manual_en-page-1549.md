

```markdown
Chapter 41 Motor Control PWM (MCPWM)
GoBack

41.3.3.2 Dead Time Generator Module

Purpose of the Dead Time Generator Module

Section 41.3.3.1 introduced several options to generate signals on PWMxA and PWMxB outputs, with a specific placement of signal edges. The required dead time is obtained by altering the edge placement between signals and by setting the signal’s duty cycle. Another option to control the dead time is to use a specialized module – Dead Time Generator.

The key functions of the Dead Time Generator module are as follows:

* Generating output signal pairs (PWMxA and PWMxB) with a dead time from a common source, which can be either the input signal PWMxA or PWMxB.
* Creating a dead time by adding delay to signal edges:
    - Rising edge delay (RED)
    - Falling edge delay (FED)
* Can generate PWM signal in various format. The typical dead time configurations are:
    - Active high complementary (AHC)
    - Active low complementary (ALC)
    - Active high (AH)
    - Active low (AL)
* This module may also be bypassed, if the dead time is configured directly in the generator module.

Shadow Register of Dead Time Generator

Delay registers RED and FED are shadowed with registers MCPWM_DTn_RED_CFG_REG and MCPWM_DTn_FED_CFG_REG. When MCPWM_GLOBAL_UP_EN is set to 1, the values saved in the shadow registers can be written to the active register at the specified time. The update method register for MCPWM_DTn_RED_CFG_REG is MCPWM_DBn_RED_UPMETHOD. The update method register for MCPWM_DTn_FED_CFG_REG is MCPWM_DBn_FED_UPMETHOD. The Software can also trigger a globally forced update bit MCPWM_GLOBAL_FORCE_UP which will prompt all registers in the module to be updated according to shadow registers. For the description of shadow registers, please see section 41.3.2.3.
```