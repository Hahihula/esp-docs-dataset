**Title:**
Chapter 23

**Subtitle:**
Pulse Count Controller (PCNT)

**Section Title:**
23.1 Overview

**Body Text:**
The pulse counter module is designed to count the number of rising and/or falling edges of an input signal.

Each pulse counter unit has a 16-bit signed counter register and two channels that can be configured to either increment or decrement the counter. Each channel has a signal input that accepts signal edges to be detected, as well as a control input that can be used to enable or disable the signal input. The inputs have optional filters that can be used to discard unwanted glitches in the signal.

The pulse counter has eight independent units, referred to as PULSE_CNT_0.

The maximum frequency of pulses supported by ESP32’s pulse counter is 40 MHz.

**Section Title:**
23.2 Functional Description

**Footer Information:**
Espressif Systems
Page number: 450
Document version and feedback link:
ESP32 TRM (Version 5.6)
Submit Documentation Feedback