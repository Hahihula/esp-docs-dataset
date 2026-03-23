
```markdown
Chapter 12 Low-Power Management

• Mode 1: Resets the system directly.

The brownout reset workflow is illustrated in the diagram below:

![Figure 12.4-3. Brownout Reset Workflow](image_path_if_available)

Registers for controlling related signals are described below:
• bod_mode0_en: LP_ANA_BOD_MODE0_INTR_ENA
• bod_mode0_rst_en: LP_ANA_BOD_MODE0_RESET_ENA
• bod_mode0_rst_sel: LP_ANA_BOD_MODE0_RESET_SEL configures the reset type:
  - 0: chip reset
  - 1: system reset

For more information regarding chip reset and system reset, please refer to Chapter 8 Reset and Clock.
• bod_mode1_sel: The first bit of LP_ANA_ANA_FIB_ENA.
• bod_mode1_rst_en: LP_ANA_BOD_MODE1_RESET_ENA

12.5 Power Modes

ESP32-C6 has four configurable PMU states. Based on the four PMU states, five power modes have been defined for the most commonly seen application scenarios. For the details, please see Table 12.5-1.
```