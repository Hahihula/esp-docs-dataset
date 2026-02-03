**Title: Chapter 39 On-Chip Sensors and Analog Signal Processing**

**Body Text:**
A touch panel consists of the following components:
- An electrode that will have a change in capacitance when touched by a finger.
- Substrate (base material) on which the protective cover, electrode, and the electrode’s connector to the channel are built.

When developing applications using the touch sensing feature, users should decide on the placement, the material, or the arrangement of the touch panel(s) during mechanical design. For more information about the design guidelines, please refer to Touch Sensor Application Note.
Touch panel can be connected to ESP32-S3 touch sensor via touch pin (channel), see Figure 39.2-1.

**Figure Caption:**
Figure 39.2-1. Touch Sensor

**Diagram Description in Image:**
The diagram shows a cross-section of the components involved with an electrode, protective cover, and substrate labeled as "Electrode," "Protective cover" (labeled C), and "Substrate." There is also mention of a chip.

**Body Text Continued:**
When users touch the protective cover, the capacitance of the electrode will increase. If the electrode is connected to one of the ESP32-S3 touch sensors (via a channel), the touch sensor will be able to detect the electrode’s change in capacitance. If the change of capacitance exceeds a certain threshold (configurable), the touch sensor can trigger an interrupt.

**Subtitle: 39.2.3 Features**

- **List Item:** 
14 touch sensors (T1 ~ T14) each with a dedicated channel that can be connected to an external touch panel. An additional touch sensor (TO) that does not have a channel is provided for noise detection purposes (see Section 39.2.8).

- **List Item:**
The touch sensors are controlled by a Touch Finite State Machine (Touch FSM). The Touch FSM can be triggered by software or a dedicated hardware timer to conduct a measurement (i.e., take a sample) on a particular touch pin.

- **List Item:** 
The Touch FSM can be configured to measure multiple touch pins in a sequential manner (scan). Scanning can be useful when multiple touch pins need to be monitored simultaneously. 

**Footer:**
Espressif Systems  
1455  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)