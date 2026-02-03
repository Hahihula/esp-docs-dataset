**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Note Section:**
For all the modes above, the position of the binary switches S4 to S8 is set to 0.

- **Mode 1**: Bypass delays on both falling edge (FED) as well as raising edge (RED)
  In this mode the dead time submodule is disabled. Signals PWMXA and PWMXB pass through without any modifications.
  
- **Mode 2-5**: Classical Dead Time Polarity Settings
  These modes represent typical configurations of polarity and should cover the active-high/low modes in available industry power switch gate drivers. The typical waveforms are shown in Figures 36.3-22 to 36.3-25.

- **Modes 6 and 7**: Bypass delay on falling edge (FED) or rising edge (RED)
  In these modes, either RED (Rising Edge Delay) or FED (Falling Edge Delay) is bypassed. As a result, the corresponding delay is not applied.

**Figure Descriptions:**
- **Figure 36.3-22**: Active High Complementary (AHC) Dead Time Waveforms
  - PWMXA Input and Output waveforms with DTRED marking.
  
- **Figure 36.3-23**: Active Low Complementary (ALC) Dead Time Waveforms
  - PWMXA Input and Output waveforms with DTFED marking.

**Footer:**
Espressif Systems, Page number 1353 ESP32-S3 TRM (Version 1.7), Submit Documentation Feedback