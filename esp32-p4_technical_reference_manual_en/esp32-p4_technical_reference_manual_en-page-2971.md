

```markdown
Chapter 60 Touch Sensor (TOUCH)

GoBack

* Configuration of individual touch sensors to operate normally in sleep mode
* Wake-up by touch sensor
* Moisture resistance
* Waterproof design

## 60.3 Architectural Overview

### 60.3.1 Touch Panel

A touch panel consists of the following components:

* Electrode: Changes in capacitance when touched by a finger.
* Substrate: The base material on which the protective cover, electrode, and the electrode’s connector to the channel are built.
* Protective cover: To physically separate the other components from the external environment.

When developing applications using the touch sensing feature, users should decide on the placement, the material, or the arrangement of the touch panels during mechanical design. For more information about the design guidelines, please refer to Touch Sensor Application Note. Touch panel can be connected to ESP32-P4 touch sensor via touch pin (channel). See Figure 60.3-1.

![Figure 60.3-1. Touch Sensor System](image)

When users touch the protective cover, the capacitance of the electrode increases. If the electrode is connected to one of the ESP32-P4 touch sensors via a channel, the touch sensor will be able to detect the electrode’s change in capacitance. If the change of capacitance exceeds the configurable threshold, the touch sensor will trigger an interrupt.
```