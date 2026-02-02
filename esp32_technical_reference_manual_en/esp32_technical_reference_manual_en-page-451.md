**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Section Header:**
23.2.1 Architecture

**Figure Caption and Diagram Description:**
- **Figure:** Figure 23.2-1. PULSE_CNT Architecture.
- The diagram shows the architecture of a pulse count controller with various components such as filters, comparators, and an adder.

**Body Text for Section 23.2.1 (Architecture):**
The text describes that each channel in the PCNT has two channels: ch0 and ch1 which are functionally equivalent; both have signal inputs connected to I/O pads with configurable counting behavior on positive or negative edges, as well as no action.

**Section Header:**
23.2.2 Counter Channel Inputs

**Body Text for Section 23.2.2 (Counter Channel Inputs):**
The text explains how the two input signals of a channel can affect the pulse counter based on control signal levels and modes:
- LCTRL_MODE and HCTRL_MODE set behavior when low or high.
- POS_MODE increases count with positive edges, NEG_MODE decreases it; setting to 1 neutralizes edge effects.

**Footer:**
Espressif Systems
451 ESP32 TRM (Version 5.6)
Submit Documentation Feedback