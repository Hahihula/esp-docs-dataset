

```markdown
Chapter 19 Power Supply Detector

GoBack

bod_mode0_en ──► Brown-out Counter ──► Int Comparator ──► bod_mode0_int  
                 │                              │  
                 ├───────────► Rst Comparator ──► bod_mode0_rst_sel ──► Chip Reset / System Reset
                 │
Brown-out Detected ──► bod_mode1_rst_en ──► S& ──► System Reset

Figure 19.3-2. Brown-out Reset Workflow

Registers for controlling related signals are described below.
*   `bod_mode0_en`: LP_ANA_BOD_MODE0_INTR_ENA
*   `bod_mode0_rst_en`: LP_ANA_BOD_MODE0_RESET_ENA
*   `bod_mode0_rst_sel`: LP_ANA_BOD_MODE0_RESET_SEL configures the reset type:
    - 0: chip reset
    - 1: system reset

For more information regarding chip reset and system reset, please refer to Chapter 7 Reset and Clock.

*   `bod_mode1_sel`: The first bit of LP_ANA_ANA_FIB_ENA.
*   `bod_mode1_rst_en`: LP_ANA_BOD_MODE1_RESET_ENA

19.3.3 Voltage Glitch Detectors

Figure 19.3-3 shows the structure of the voltage glitch detectors.

Espressif Systems
757
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```