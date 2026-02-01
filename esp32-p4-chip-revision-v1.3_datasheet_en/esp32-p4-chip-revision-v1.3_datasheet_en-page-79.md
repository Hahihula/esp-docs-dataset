**Title: Functional Description**

- **Subtitle:** Pin Assignment

The pins of the analog voltage comparator are multiplexed with GPIO51-GPIO52, GPIO53-GPIO54, the interface of one ADC controller, and the third RMII interface of EMAC.

---

**Title: 4.2.3.5 Voice Activity Detection (VAD)**

ESP32-P4 integrates a Voice Activity Detection (VAD) module. This module facilitates the hardware implementation of the first-stage algorithm for voice wake-up and other multimedia functions. Additionally, it provides hardware support for low-power voice wake-up solutions.

**Subtitle:** Feature List

- VAD algorithm processes voice data frame by frame, with each frame containing 256 data points. The data sampling rate is 8 kHz, and the bit width is 16 bits
- 2 KB buffer that stores up to four frames of data
- Independent system wake-up source
- Configurable interrupt sources
- Flexible configuration of algorithm parameters

**Subtitle:** Pin Assignment

The VAD module does not directly interact with IOs, so it has no pins assigned.

---

**Footer:**
Espressif Systems  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)