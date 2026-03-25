

```markdown
## 36.3.3.2 Dead Time Generator Module

### Purpose of the Dead Time Generator Module

Section 36.3.3.1 introduced several options to generate signals on PWMxA and PWMxB outputs, with a specific placement of signal edges. The required dead time is obtained by altering the edge placement between signals and by setting the signal’s duty cycle. Another option to control the dead time is to use a specialized module – Dead Time Generator.

The key functions of the Dead Time Generator module are as follows:

* Generating signal pairs (PWMxA and PWMxB) with a dead time from a single PWMxA input
* Creating a dead time by adding delays to signal edges:
    * Rising edge delays (RED)
    * Falling edge delays (FED)
* Configuring the signal pairs to be:
    * Active high complementary (AHC)
    * Active low complementary (ALC)
    * Active high (AH)
    * Active low (AL)
* This module may also be bypassed, if the dead time is configured directly in the generator module.

### Shadow Register of Dead Time Generator

Delay registers RED and FED are shadowed with registers `MCPWM_DTx_RED_CFG_REG` and `MCPWM_DTx_FED_CFG_REG`. When `MCPWM_GLOBAL_UP_EN` is set to 1, the values saved in the shadow registers can be written to the active register at a specified time. The update method register for `MCPWM_DTx_RED_CFG_REG` is `MCPWM_DTx_RED_UPMETHOD`. The update method register for `MCPWM_DTx_FED_CFG_REG` is `MCPWM_DTx_FED_UPMETHOD`. The Software can also trigger a globally forced update bit `MCPWM_GLOBAL_FORCE_UP` which will prompt all registers in the module to be updated according to shadow registers. For the description of shadow registers, please see section 36.3.2.3.
```