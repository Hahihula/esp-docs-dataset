**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Diagram Description (Figure):**
- **Figure Title:** Figure 39.2-1, Touch FSM Structure.
- The diagram shows a block diagram with various components such as Timer, Software, CPU, Denoise unit, Work unit, Filter, and connections between them.

**Text Content:**

The following points describe the various modules of the Touch FSM:

- **SCAN_CTRL:** selects the touch pin to measure when in scan mode.
- **WORK_UNIT:** drives a selected touch pin during a measurement.
- **DENOISE_UNIT:** has a nearly identical structure to the WORK_UNIT, but is connected to an internal touch sensor (TO). The measurements from TO can be used by the other touch sensors to correct for noise (see section 39.2.8).
- Filter module: if enabled, each touch sensor can filter a series of measurements via an infinite impulse response (IIR) filter. The filtered value will be returned as the sampled value instead (see section 39.2.7).

**Subtitle and Section Numbering:** 
39.2.6.1 Measurement Process

**Body Text:**
A single measurement of a touch pin involves the following process:

1. **The Touch FSM selects the touch sensor to be measured. The relevant signals are routed to that touch sensor.**
2. **The Touch FSM drives the “START” signal to the touch sensor initiating the measurement. Internally, the Touch FSM starts an internal “touch counter” to time the duration of the measurement.**
3. **A "pulse counter" in the Touch FSM will increment on each pulse received from the touch sensor’s “OUT” signal.**
4. When the pulse counter reaches the count threshold set in RTC_CNTL_TOUCH_MEAS_NUM, the measurement is complete. The “START” signal is de-asserted, and the touch counter is stopped.

**Footer:**
Espressif Systems
1459 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback