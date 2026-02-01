**Title:**
4 Boot Configurations

**Figure Caption and Description:**
- **Figure:** Figure 4-2.
- **Caption:** Visualization of Timing Parameters for Power-up and Reset.

**Table Title and Content:**
- **Table Name:** Table 4-6. 
- **Title:** Description of Timing Parameters for Power-up and Reset
- **Columns:** Parameter, Description, Min (µs)
- **Rows:**
  - t_STBL: Time reserved for the power rails of VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_RTC_IO, and VDD3P3_CPU to stabilize before the CHIP PU pin is pulled high to activate the chip. Description states "Time observed for the power rails of VDDA, VDD3P3, VDD3P3_RTC, VDD3P3_RTC_IO, and VDD3P3_CPU to stabilize before the CHIP PU pin is pulled high to activate the chip." Min (µs) = 50.
  - t_RST: Time reserved for CHIP PU to stay below V_IL-nRST to reset the chip. Description states "Time reserved for CHIP PU to stay below V_IL-nRST to reset the chip" with a reference "(see Table 5-3)". Min (µs) = 50.

**Footer Information:** 
- Company: Espressif Systems
- Document Version and Feedback Link:
  - ESP32-S2-SOLO-2 & SOLO-2U Datasheet v1.3
  - Submit Documentation Feedback