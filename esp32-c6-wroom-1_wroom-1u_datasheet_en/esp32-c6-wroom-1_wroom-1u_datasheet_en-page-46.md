**Title:**
12 Product Handling

**Subtitle and Body Texts with Structure Indication (e.g., headings, lists):**

- **12.1 Storage Conditions**
  - The products sealed in moisture barrier bags (MBB) should be stored in a non-condensing atmospheric environment of <40 °C and 90%RH. The module is rated at the moisture sensitivity level (MSL) of 3.
  - After unpacking, the module must be soldered within 168 hours with the factory conditions ±5 °C and 60%RH. If these above conditions are not met, the module needs to be baked.

- **12.2 Electrostatic Discharge (ESD)**
  - Human body model (HBM): ±2000 V
  - Charged-device model (CDM): ±500 V

- **12.3 Reflow Profile**
  - Solder the module in a single reflow.
    - Peak temperature: 235 – 250 °C
    - Peak time: 30 – 70 s
    - Soldering time: > 30 s
    - Solder type: Sn-Ag-Cu (SAC305) lead-free solder

**Diagram Description and Labels in Markdown Format**

- **Figure Caption:** Figure 12-1. Reflow Profile
- **Temperature Axis Label:** Temperature (°C)
- **Time Axis Label:** Time (s)

**Reflow Profile Details:**
- Ramp-up:
  - Range: 25 – 150 °C, Rate: >60°C/s to <90°C/s

- Preheating:
  - Range: 150 – 200 °C
  - Time: ~3 s
  
- Soldering:
  - Range: >217 °C 
  - Time: ~60–90 s

- Cooling:
  - Range: <180 °C, Rate: ~5°C/s to ~1°C/s

**Footer Information**
- Company Name:** Espressif Systems
- Document Version and Feedback Link:** ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4 | Submit Documentation Feedback