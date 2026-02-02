**Title:**
4 Boot Configurations

**Figure Description and Caption:**
- **Figure:** Figure 4-2 shows a "Visualization of Timing Parameters for Power-up and Reset".
- The figure includes labels such as VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_RTC_IO, VDD3P3_CPU.

**Table Description:**
- **Title:** Table 4-6. "Description of Timing Parameters for Power-up and Reset".
  
| Parameter | Description | Min (µs) |
|-----------|-------------|----------|
| t_STBL    | Time reserved for the power rails of VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_RTC_IO, and VDD3P3_CPU to stabilize before the CHIP PU pin is pulled high to activate the chip. | 50 |
| t_RST     | Time reserved for CHIP PU to stay below V_IL-nRST to reset the chip (see Table 5-3). | 50 |

**Footer:**
- "Espressif Systems"
- Page number and document version information at the bottom right corner:
  - ESP32-S2-MINI-2 & MINI-2U Datasheet v1.3
  - Submit Documentation Feedback

This layout provides a clear overview of timing parameters necessary for power-up and reset processes in electronic components, specifically related to VDDA (power supply voltage), VDD3P3 (power rails or domains specific to the chip's operation). The table lists two key time-related parameters: t_STBL and t_RST.