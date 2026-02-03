**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** (Located at top right corner)

---

**Table of Touch Sensing Signals by Pin:**

| T11    | GPIO11 |
| T12    | GPIO12 |
| T13    | GPIO13 |
| T14    | GPIO14 |

---

**Section Title and Subtitle:**
39.2.5 Touch Sensors Operating Principle and Signals

**Figure Caption (with Figure):**
- **Figure 39.2-2:** Touch Sensor Operating Principle
- The figure shows two graphs labeled "START" on the left side, with time 't' marked along both axes of each graph.

**Body Text:**

Figure 39.2-2 illustrates the operating principle of a touch sensor. When a touch pin is touched (or positioned proximate to finger), the capacitance of the touch pin will increase. A touch sensor is able to detect a change in capacitance of a touch pin.
To measure a change in capacitance in the touch pin, a touch sensor will rapidly charge and discharge the touch pin between a high and low voltage (named “DREFH” and “DERFL” respectively) using a fixed current source. If the touch pin is touched, the touch pin’s capacitance will increase thus will take longer to charge and discharge. By measuring the time taken to charge/discharge the touch pin in a fixed number of cycles, it can be deduced whether the touch pin is touched or not.
Each touch sensor will output an “OUT” signal that consists of pulses generated on each voltage swing. A single measurement primarily consists of a touch sensor charging/discharging the touch pin a fixed “N” cycles, and measuring the time taken for “OUT” signal to generate “N” pulses.

---

**Footer:**
Espressif Systems
1457 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

(Note: The "GoBack" link is a navigation element in software or web applications, not part of the document content.)