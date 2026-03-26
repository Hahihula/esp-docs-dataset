

# Chapter 60

## Touch Sensor (TOUCH)

ESP32-P4 has 14 capacitive touch sensor units, each of which can be connected to an external touch panel via a touch pin (GPIO pin) to constitute a touch sensor system. The ESP32-P4 touch sensor system is mainly used in human-computer interactions to detect finger touch or proximity. It also features moisture resistance and waterproof design.

### 60.1 Terminology

To better illustrate the functions of capacitive touch sensors, the following terms are used in this section.

| Term             | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| Touch Sensor     | Touch-related internal sensing circuitry.                                   |
| Touch Pin        | Pins with touch sensing feature.                                            |
| Touch Panel      | The external device connected to touch sensor via channel (touch pin) to detect finger touch. |
| Touch Sensor System | Capacitive touch sensing system, consisting of touch sensor, touch pin, traces, and touch panel. |

**Note:**  
In subsequent description, “touch panel is sampled/scanned/measured” indicates the same action to touch pin, i.e. “*touch pin is sampled/scanned/measured*”.

### 60.2 Feature List

The ESP32-P4 touch sensor has the following features:

- Detection of 14 capacitive touch pins
- Sampling triggered by software or dedicated hardware timer
- Two sampling methods:
    - Pulses from the touch pins used as clock signals to count the sampling period
    - Pulses from the touch pins used as digital signals; sample the rising edge of the digital signal with the system clock to count the sampling period
- Scan mode, supporting sequential sampling of multiple touch pins by configuring the Touch FSM.
- Timeout mechanism to monitor channel abnormality
- Frequency hopping to increase the anti-interference of detection
- Proximity sensing mode with up to three configurable channels