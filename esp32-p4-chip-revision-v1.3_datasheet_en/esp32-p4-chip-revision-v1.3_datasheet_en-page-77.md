**Title: Functional Description**

**Body Text:**
can be detected. The touch sensing performance can be further enhanced by the waterproof design, detection of frequency hopping, and digital filtering feature.

**Subtitle: Feature List**

- Detection of 14 capacitive touch pins
- Sampling triggered by software or dedicated hardware timer

**Subsection Title: Two sampling methods:**
- Pulses from the touch pins used as clock signals to count the sampling period
- Pulses from the touch pins used as digital signals; sample the rising edge of the digital signal with the system clock to count the sampling period

- Scan mode, supporting sequential sampling of multiple touch pins by configuring the Touch FSM.
- Timeout mechanism to monitor channel abnormality
- Frequency hopping to increase the anti-interference of detection
- Proximity sensing mode with up to three configurable channels
- Configuration of individual touch sensors to operate normally in sleep mode
- Wake-up by touch sensor
- Moisture resistance
- Waterproof design

**Subtitle: Pin Assignment**

The pins of the touch sensor are multiplexed with GPIO2–GPIO15, LP_GPIO2–LP_GPIO15, LP_UART interface, and one four-line interface of SPI2. When the pins are configured for the analog function, the multiplexed digital functions are disabled.

**Subtitle: 4.2.3.2 Temperature Sensor (TSENS)**

ESP32-P4 provides a temperature sensor for real-time monitoring of temperature changes within the chip. The sensor converts analog voltage to digital values and provides compensation for temperature offsets.

**Subtitle: Feature List**

- Software-triggered temperature measurement, which once triggered, the sensor continuously measures temperature. Software can read the data at any time.
- Hardware-triggered automatic temperature monitoring, supporting two wake-up modes
- Configurable temperature offset based on the application scenario for improved accuracy
- Configurable temperature measurement range
- Support for Event Task Matrix (ETM)-related events and tasks

**Footer:**
Espressif Systems  
77  
ESP32-P4 Series Datasheet v0.6  
Submit Documentation Feedback