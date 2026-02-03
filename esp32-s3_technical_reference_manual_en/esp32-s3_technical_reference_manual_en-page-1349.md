**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**
Figure 36.3-20 shows a waveform of CNTU software-force events. UTEZ events are selected as triggers for CNTU software-force events. CNTU is used to force the PWMx output low. Forcing on PWMxA is disabled.

**Diagram Labels and Descriptions:**
- Period = 6
- A = 3

**Waveform Components (from top to bottom):**
1. **PWM timer**: Shows a step waveform with steps labeled from '0' through '6'.
2. **UTEP, UTEZ, UTEA**: These are different signal lines that show various states over time.
3. **CNTU force event**: Indicates points where CNTU forces occur on the PWMxA line.

**Additional Labels:**
- "PWMxA" and "PWMxB": Represent two separate signals or outputs being controlled by the waveform events shown in the diagram.
- Arrows pointing to specific times on the timeline, indicating when certain actions (like forcing a signal low) are triggered based on CNTU force event timing.

**Caption for Diagram:**
Figure 36.3-20. Example of a CNTU Software-Force Event on PWMxB

**Footer Information:**
Espressif Systems
1349 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback