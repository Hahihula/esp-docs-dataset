**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Subtitle:**
36.3.3.2 Dead Time Generator Submodule

**Section Title:**
Purpose of the Dead Time Generator Submodule

**Body Text:**
Several options to generate signals on PWMXA and PWMXB outputs, with a specific placement of signal edges, have been discussed in section 36.3.3.1. The required dead time is obtained by altering the edge placement between signals and by setting the signal’s duty cycle. Another option is to control the dead time using a specialized submodule – the Dead Time Generator.

The key functions of the dead time generator submodule are as follows:

- Generating signal pairs (PWMXA and PWMXB) with a dead time from a single PWMXA input
- Creating a dead time by adding delay to signal edges:
  - Rising edge delay (RED)
  - Falling edge delay (FED)
- Configuring the signal pairs to be:
  - Active high complementary (AHC)
  - Active low complementary (ALC)
  - Active high (AH)
  - Active low (AL)

This submodule may also be bypassed, if the dead time is configured directly in the generator submodule.

**Subsection Title:**
Dead Time Generator’s Shadow Registers

**Body Text:**
Delay registers RED and FED are shadowed with registers MCPWM_DTRED_CFG_REG and MCPWM_DTXFED_CFG_REG. When MCPWM_GLOBAL_UP_EN is set to 1, the shadow registers can be written to the active register at specified time. The update method register for MCPWM_DTRED_CFG_REG is MCPWM_DT_RED_UPMETHOD. The update method register for MCPWM_DTRED_CFG_REG is MCPWM_DT_FED_UPMETHOD. The Software can also trigger a globally forced update bit MCPWM_GLOBALFORCE_UP which will prompt all registers in the module to be updated according to shadow registers. For the description of shadow registers, please see section 36.3.2.3.

**Subsection Title:**
Highlights for Operation of the Dead Time Generator

**Body Text:**
Options for setting up the dead-time submodule are shown in Figure 36.3-21.

**Footer Information:**
Espressif Systems
Page number: 1350
Document version and type information at bottom right corner (not fully visible).