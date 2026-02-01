Title: Revision History

Table:
- Column Headers: Date, Version, Release notes
- Row Entries (partial):
  - "2025-10-23 v0.6"
    - Updated Figure ESP32-P4 Functional Block Diagram in Section Product Overview.
    - Section 3 Boot Configurations: Updated Figure 3-1 Visualization of Timing Parameters for the Strapping Pins
    - Chapter 4.1.2.1 GDMA Controller (GDMA-AHB, GDMA-AXI): Updated the accessible memory type for GDMA-AHB
    - Updated description in Section 4.1.3 System and Memory, 4.2.2.14 SD/MC Host Controller (SDHOST) and 4.2.2.12 Ethernet Media Access Controller (EMAC)
    - Section 5.2 Recommended Operating Conditions: Updated the recommended minimum input voltage of VDD_BAT to be 2.5 V
    - Section 5.5 ADI Characteristics:
      - Corrected a typo in Table 5-6 ADC Calibration Results: the accuracy range is –12 to 12.
      - Corrected a typo in Table 5-7 Current Consumption in Active and Low-power Modes: At a frequency of 90 MHz in dual-core while(1) loop operation when all peripheral clocks are enabled, the power consumption should be 53 mA
    - Corrected typos in Section Appendix A – ESP32-P4 Consolidated Pin Overview: the pin providing power for CHIP_PU should be VDD_BAT, no weak pull-up resistance for GPIO36 at reset

Footer:
- "Preliminary release"
- Date and Version Information (partially visible): 2025-06-03 v0.5
- Company Name: Espressif Systems
- Document Title: ESP32-P4 Series Datasheet v0.6
- Link Texts:
  - "Submit Documentation Feedback"