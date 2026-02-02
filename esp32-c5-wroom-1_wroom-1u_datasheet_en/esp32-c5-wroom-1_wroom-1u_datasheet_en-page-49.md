**Title:**
Figure 8-2. ESP32-C5-WROOM-1U Schematics

**Body Text (within diagram):**

- For modules with embedded PSRAM, SPICS1 is connected to the embedded PSRAM and is not available for other uses.
  
- The values of C1 and C2 vary with the selection of the crystal. 
  - The value of R1 varies with the actual PCB board; R1 could be a fixed resistor or an adjustable trimmer capacitor, but in most cases it's suggested to use its resistance is about 47kΩ.

- Dual Band Diplexer
  - RF 2.4G&5G: Single-ended 50ohm

**Additional Notes (within diagram):**
- Add a stub to the ground pad.
- The values of C23, L2, C24, L3, C25, LS and CB vary with actual PCB board.

**Legend/Key within Diagrams:** 
- NC: No component
- GND

**Side Text (vertical):**
Espressif Systems  
Submit Documentation Feedback ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8 PRELIMINARY  

**Page Number and Section Indicator on the Right Side of Diagram:** 
Module Schematics 8