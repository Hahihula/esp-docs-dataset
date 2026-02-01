**Title:**
4 Boot Configurations

**Figure Description and Caption:**
- **Figure:** Figure 4-2 shows a "Visualization of Timing Parameters for Power-up and Reset".
- The figure includes labels such as VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_CPU.
- There are timing parameters labeled \( t_{STBL} \) (Time to Stable Level), indicating the time observed before stabilization.

**Table Description:**
- **Title:** Table 4-6. "Description of Timing Parameters for Power-up and Reset".
- The table has columns titled Parameter, Description, Min (\(\mu\)s).
  
| Parameter | Description                                                                                   | Min (\(\mu\)s) |
|-----------|--------------------------------------------------------------------------------------------------|----------------|
| \( t_{STBL} \) | Time observed for the power falls of VDDA, VDD3P3, VDD3P3_RTC, and VDD3P3_CPU to stabilize before the CHIP_EN pin is pulled high to activate the chip. | 50             |
| \( t_{RST} \) | Time reserved for CHIP_EN to stay below \( V_{IL_nRST} \) to reset the chip (see Table 6-3).     | 50             |

**Footer:**
- "Espressif Systems"
- Page number and document version information:
  - ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1
  - Submit Documentation Feedback

This layout provides a clear overview of the timing parameters necessary for power-up and reset operations in electronic systems, as specified by Espressif Systems' datasheet documentation.