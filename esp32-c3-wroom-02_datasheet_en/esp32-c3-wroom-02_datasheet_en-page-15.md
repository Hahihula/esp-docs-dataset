**Title:**
4 Boot Configurations

**Figure Caption and Description:**
- **Figure:** Figure 4-2. Visualization of Timing Parameters for Power-up and Reset.
- The figure shows a timing diagram with labels such as VDDA, VDD3P3, VDD3P3_RTC, and VDD3P3_CPU.

**Table Title and Content:**
- Table 4-6. Description of Timing Parameters for Power-up and Reset
  - **Parameter | Description | Min (µs)**
    - t_STBL | Time reserved for the power rails of VDDA, VDD3P3, VDD3P3_RTC, and VDD3P3_CPU to stabilize before the CHIP_EN pin is pulled high to activate the chip. | 50
    - t_RST | Time reserved for CHIP_EN to stay below V_IL_nRST to reset the chip (see Table 6-3). | 50

**Footer:**
- Espressif Systems, Page number and document version information:
  - "ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6"
  - Link to submit documentation feedback.

(Note: The text in the figure is not fully transcribed due to its graphical nature.)