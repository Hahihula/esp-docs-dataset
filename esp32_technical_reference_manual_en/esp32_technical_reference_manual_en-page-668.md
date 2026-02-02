**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Body Text:**
CNTU software-force events. CNTU is used to force the PWMx*B output low. Forcing on PWMxA is disabled.

**Diagram Description and Labels:**
- The diagram shows a timing waveform with labels such as "Period = 6", "A = 3".
- It includes sections labeled "PWM timer" showing steps from '0' through '6'.
- There are various lines indicating different signals like UTEP, UTEZ, UTEA.
- A section is marked for CNTU force event with an arrow pointing to a specific point on the waveform.

**Figure Caption:**
Figure 29.3-20. Example of a CNTU Software-Force Event on PWMxB

**Subsection Title and Subtitle:**
29.3.3.2 Dead Time Generator Submodule
Purpose of the Dead Time Generator Submodule

**Body Text (continued):**
Several options to generate signals on PWMxA and PWMxB outputs, with a specific placement of signal edges, have been discussed in section 29.3.3.1. The required dead time is obtained by altering the edge placement between signals and by setting the signal’s duty cycle. Another option is to control the dead time using a specialized submodule – the Dead Time Generator.

The key functions of the dead time generator submodule are as follows:

**Footer:**
Espressif Systems
668 ESP32 TRM (Version 5.6)
Submit Documentation Feedback