

```markdown
Chapter 18 Power Supply Detector

GoBack

Figure 18.3-2. Brown-out Reset Workflow

Registers for controlling related signals are described below.

*   `bod_mode0_en`: LP_ANA_BOD_MODEO_INTR_ENA
*   `bod_mode0_rst_en`: LP_ANA_BOD_MODEO_RESET_ENA
*   `bod_mode0_rst_sel`: LP_ANA_BOD_MODEO_RESET_SEL configures the reset type after the brown-out detector is triggered in mode 0:
    -   0: chip reset
    -   1: system reset

For more information regarding chip reset and system reset, please refer to Chapter 7 Reset and Clock.

*   `bod_mode1_sel`: The first bit of LP_ANA_ANA_FIB_ENA
*   `bod_mode1_rst_en`: LP_ANA_BOD_MODE1_RESET_ENA

18.3.3 Voltage Glitch Detectors

Figure 18.3-3 shows the structure of the voltage glitch detectors.
```
```plaintext
Espressif Systems                          574                           ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```