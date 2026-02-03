**Chapter Title:**
Chapter 39

**Section Titles and Subsections with Content:**

1. **Title:** On-Chip Sensors and Analog Signal Processing

2. **Subtitle (39.1): Overview**
   - ESP32-S3 provides the following on-chip sensors and signal processing peripherals:
     - Fourteen capacitive touch sensors that can be used to detect finger touches from 14 channels.
       The touch sensors can also be configured to be moisture tolerant, and support Water Rejection capabilities. A proximity sensing mode is also supported.

   - One temperature sensor for measuring the internal temperature of the ESP32-S3 chip.

   - Two 12-bit Successive Approximation ADCs (SAR ADCs) controlled by five dedicated controllers that can input analog signals from total of 20 channels.
     The SAR ADCs can operate in a high-performance mode or a low-power mode.

3. **Subtitle (39.2): Capacitive Touch Sensors**

4. **Subsection Title:** Terminology

   - To better illustrate the functions of capacitive touch sensors, the following terms are used in this section.
     - Touch pin: GPIO pins provided by ESP32-S3 with touch sensing feature.

     - Touch sensor: touch-related internal sensing circuitry integrated in ESP32-S3.

     - Touch panel: the external device connected to touch sensor via channel (touch pin) to detect finger touch.

     - Touch sensor system: ESP32-S3 capacitive touch sensing system, consisting of touch sensor, touch pin, traces, and touch panel.
   
   **Note:** In subsequent description, “touch panel is sampled/scanned/measured” indicates the same action to touch pin, i.e., "touch pin is sampled/scanned/measured".

5. **Subsection Title (39.2.2): Overview**
   - ESP32-S3 provides built-in touch sensors, which can be connected to external touch panel via touch pin (GPIO pin) to constitute a touch sensor system.
     Such system can be applied in human-computer interaction scenarios to detect finger touch or proximity.

**Footer:**
- Page number and document version information:
  - Espressif Systems
  - Document page count/numbering indicator "1454"
  - ESP32-S3 TRM (Version 1.7)
  - Submission Feedback link