**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** [GoBack](#)

**Body Text:**

- **Generating signal pairs (PWMXA and PWMXB) with a dead time from a single PWMXA input**
  
- Creating a dead time by adding delay to signal edges:
  - Rising edge delay (RED)
  - Falling edge delay (FED)

- Configuring the signal pairs to be:
  - Active high complementary (AHC)
  - Active low complementary (ALC)
  - Active high (AH)
  - Active low (AL)

**Note:**
This submodule may also be bypassed, if the dead time is configured directly in the generator submodule.

**Subheading:** Dead Time Generator’s Shadow Registers

Delay registers RED and FED are shadowed with registers PWM_DTx_RED_CFG_REG and PWM_DTx_FED_CFG_REG. For the description of shadow registers, please see section 29.3.2.3.

**Subheading:** Highlights for Operation of the Dead Time Generator

Options for setting up the dead-time submodule are shown in Figure 29.3-21.

**Figure Caption:**
Figure 29.3-21 Options for Setting up the Dead Time Generator Submodule
SO-8 in the figure above are switches controlled by registers PWM_DTx_CFG_REG shown in Table 29.3-5.
- **Diagram Description:** The diagram shows a schematic with inputs labeled as "PWMXA Input" and "PWMXB Input," along with various logic gates (S0, S1) connected to outputs marked as "PWMXA Output" and "PWMXB Output." There are also labels for Rising Edge Delay ("Rising Edge Delay") and Falling Edge Delay ("Falling Edge Delay").

**Table Caption:**
Table 29.3-5 Dead Time Generator Switches Control Registers

| Switch | Register |
|--------|----------|
| S0     | PWM_DTx_B_OUTBYPASS |

**Footer Information:** 
Espressif Systems
669 ESP32 TRM (Version 5.6)
Submit Documentation Feedback