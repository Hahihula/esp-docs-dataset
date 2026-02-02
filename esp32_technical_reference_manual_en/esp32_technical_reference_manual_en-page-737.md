**Title:**
Chapter 31

**Subtitle:**
On-Chip Sensors and Analog Signal Processing

**Section Title:**
31.1 Introduction

**Body Text:**
ESP32 has a capacitive touch sensor with up to 10 inputs.

The processing of analog signals is done by two successive approximation ADCs (SAR ADC). There are five controllers dedicated to operating ADCs. This provides flexibility when it comes to converting analog inputs in both high-performance and low-power modes, with minimum processor overhead.
ESP32 is also capable of generating analog signals, using two independent DACs and a cosine waveform generator.

**Section Title:**
31.2 Capacitive Touch Sensor

**Subsection Title:**
31.2.1 Introduction

**Body Text:**
A touch-sensor system is built on a substrate which carries electrodes and relevant connections under a protective flat surface; see Figure 31.2-1. When a user touches the surface, the capacitance variation is triggered and a binary signal is generated to indicate whether the touch is valid.

**Image Description with Caption:**
Figure 31.2-1. Touch Sensor

**Section Title:**
31.2.2 Features

**Bullet Points:**
- Up to 10 capacitive touch pads / GPIOs
- The sensing pads can be arranged in different combinations, so that a larger area or more points can be detected.

**Footer Information:**
Espressif Systems  
737  
ESP32 TRM (Version 5.6)  

**Link Text at the top right corner:** GoBack

**Link text below footer information:** Submit Documentation Feedback