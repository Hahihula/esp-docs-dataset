**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** (Located at top right corner)

**Body Text with Bullet Points:**

- Up to three channels can be configured with proximity mode.
- To determine whether a touch pin has been touched, the following touch-detection methods are supported:
  - Polling of touch sensor samples via software.
  - Built-in hardware algorithm.

Touch sensors can operate whilst the CPU is in sleep mode.  
Support ESP32-S3 low-power operation in the following scenarios:  
- Touch pins can be configured as a wakeup source when the CPU is in Deep-sleep (see RTC_CNTL_TOUCH_SLP_RAD). If the RTC Peripherals power domain is turned off (refer to Table 10.4-1), then only one touch sensor pin can be configured as a wakeup source.
- Touch pins can be controlled by the ULP coprocessor. The ULP coprocessor can be programmed to scan multiple touch pins. If a particular touch threshold is reached, the ULP coprocessor can wake up the main CPU.

**Subpoints under low-power operation:**
- Moisture tolerance (mitigate the effect of small water droplets).
- Water Rejection (detect if the sensor array surface is covered in water and trigger a shut down).
- Support internal noise filtering

**Note Section:**  
ESP32-S3 Touch Sensor has not passed the Conducted Susceptibility (CS) test for now, and thus has limited application scenarios.

**Subheading:**
39.2.4 Capacitive Touch Pins

**Body Text under Subheading:**
ESP32-S3 provides 14 capacitive touch sensors (T1 ~ T14), each of which is connected to the chip’s pin to monitor finger touch from the external environment. TO is not connected to the external environment, and is used to detect noise inside the chip (see section 39.2.8). The touch sensor to chip pin mappings are shown in Table 39.2-1.

**Table Title:**
Table 39.2-1. ESP32-S3 Capacitive Touch Pins

| Touch Sensing Signal | Pin |
|----------------------|-----|
| TO                   | Internal channel, not connect to a GPIO |
| T1                   | GPIO1 |
| T2                   | GPIO2 |
| T3                   | GPIO3 |
| T4                   | GPIO4 |
| T5                   | GPIO5 |
| T6                   | GPIO6 |
| T7                   | GPIO7 |
| T8                   | GPIO8 |
| T9                   | GPIO9 |
| T10                  | GPIO10 |

**Footer:**
Espressif Systems  
Page number 1456 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback