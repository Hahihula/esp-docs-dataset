**Title:**
12 Product Handling

**Subtitle and Body Texts with Details:**

**12.1 Storage Conditions**
The products sealed in moisture barrier bags (MBB) should be stored in a non-condensing atmospheric environment of < 40 °C and 90%RH. The module is rated at the moisture sensitivity level (MSL) of 3.

After unpacking, the module must be soldered within 168 hours with the factory conditions 25±5 °C and 60%RH. If the above conditions are not met, the module needs to be baked.

**12.2 Electrostatic Discharge (ESD)**
- Human body model (HBM): ±2000 V
- Charged-device model (CDM): ±500 V

**12.3 Reflow Profile**
Solder the module in a single reflow.
- Peak temperature: 235 – 250 °C
- Peak time: 30 – 70 s
- Soldering time: > 30 s
- Solder type: Sn-Ag-Cu (SAC305) lead-free solder

**Figure Description and Details in the Diagram**
- Title of Figure: Reflow Profile
- Temperature vs. Time Graph:
  - Y-axis labeled "Temperature (°C)" ranging from approximately 12 to above 250.
  - X-axis is not explicitly mentioned but represents time, with specific ranges for different phases indicated below.

**Phases in the Reflow Process:**
- Ramp-up
  - Temperature range: 25 – 150 °C (60°C/s)
- Preheating
  - Temperature range: 150 – 200 °C (60°C/s to > 90 s for cooling phase, which is not explicitly labeled but can be inferred from the graph's shape and direction change around this area.)
- Soldering
  - Temperature peak between approximately 235 – 250 °C.
- Cooling
  - Temperature range: <180 °C (negative slope indicating cooling phase, with a rate of ~5 to -1°C/s)

**Footer Information**
Espressif Systems  
Page number and document reference at the bottom:
48  
Submit Documentation Feedback

**Document Reference in Footer:**  
ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6