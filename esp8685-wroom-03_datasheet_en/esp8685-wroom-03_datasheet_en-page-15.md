**Title:**
4 Boot Configurations

**Figure Description and Caption:**
- **Figure:** Figure 4-2 shows a "Visualization of Timing Parameters for Power-up and Reset".
- The figure includes labels such as VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_CPU.
- There are timing parameters labeled \( t_{STBL} \) (Time to Stable Level), indicating the time observed before stabilization.

**Table Description:**
- **Title:** Table 4-6. Description of Timing Parameters for Power-up and Reset
- The table has columns titled "Parameter", "Description", and "Min (\(\mu\)s)".
- Rows include:
  - Parameter: \( t_{STBL} \), Description: Time observed before the power rails VDDA, VDD3P3, VDD3P3_RTC, and VDD3P3_CPU to stabilize; Min Value is 50 µs
  - Parameter: \( t_{RST} \), Description: Time reserved for CHIP_EN to stay below \( V_{IL_nRST} \) to reset the chip (see Table 6-3); Min Value is also 50 µs

**Footer Information:**
- "Espressif Systems"
- Page number and document version information at the bottom right corner:
  - ESP8265-WROOM-03 Datasheet v1.5
  - Submit Documentation Feedback link