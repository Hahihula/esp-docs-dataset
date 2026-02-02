**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** (Hyperlink)

**Body Text:**

- The touch pad sensing process is under the control of a hardware-implemented finite-state machine (FSM) which is initiated by software or a dedicated hardware timer.
  
- Information that a pad has been touched can be obtained:
  - by checking touch-sensor registers directly through software,
  - from an interrupt triggered by a touch detection, 
  - by waking up the CPU from deep sleep upon touch detection.

- Support for low-power operation in the following scenarios:
  - CPU waiting in deep sleep and saving power until touch detection and subsequent wake up
  - Touch detection managed by the ULP coprocessor. The user program in ULP coprocessor can trigger a scanning process by checking and writing into specific registers, in order to verify whether the touch threshold is reached.

**Note:**
ESP32 Touch Sensor has not passed the Conducted Susceptibility (CS) test for now, and thus has limited application scenarios.

**Subsection Title:** 31.2.3 Available GPIOs

**Table Description:**
All 10 available sensing GPIOs (pads) are listed in Table 31.2-1.
(Table title: "Table 31.2-1. ESP32 Capacitive Sensing Touch Pads")

| Touch Sensing Signal Name | Pin Name |
|---------------------------|----------|
| T0                       | GPIO4    |
| T1                       | GPIO0    |
| T2                       | GPIO2    |
| T3                       | MTD0     |
| T4                       | MTCK     |
| T5                       | MTDI     |
| T6                       | MTMS     |
| T7                       | GPIO27   |
| T8                       | 32K_XN   |
| T9                       | 32K_XP   |

**Subsection Title:** 31.2.4 Functional Description

The internal structure of the touch sensor is shown in Figure 31.2-2. The operating flow is shown in Figure 31.2-3.

The capacitance of a touch pad is periodically charged and discharged. The chart "Pad Voltage" shows the charge/discharge voltage that swings from DREFH (reference voltage high) to DREFL (reference voltage low). During each swing, the touch sensor generates an output pulse, shown in the chart as "OUT". The swing slope is different when the pad is touched (high capacitance) and when it is not (low capacitance).

**Footer:**
Espressif Systems

Page Number: 738
Document Version: ESP32 TRM (Version 5.6)

**Feedback Link:** Submit Documentation Feedback