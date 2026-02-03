**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Section with Bullet Points (39.2.10.2): Water Rejection**

- Set the drive strength of touch sensor 14 by RTC_CNTL_TOUCH_BUFDRAW.
- Enable touch sensor 14 to be used for moisture tolerance feature by setting RTC_CNTL TOUCH_SHIELD_PAD_EN.

**Subsection Title:**
39.2.10.2

**Body Text under Subsection (Water Rejection):**

When the sensor array becomes wet, most (if not all) of the touch pads will become unusable due to the false detection of touches.
Configure RTC_CNTL TOUCH_OUT_RING to select one of the touch pads to be used for water rejection feature.

**Subsection Title:**
39.3 SAR ADCs

**Subsection with Subtitle and Figure Reference (39.3.1 Overview):**

- **Subtitle:** 39.3.1 Overview
- ESP32-S3 integrates two 12-bit SAR ADCs, which are able to measure analog signals from up to 20 pins. See Figure 39.3-1.

**Figure Title:**
Figure 39.3-1

**Diagram Description (Analog Domain and Digital Domain):**

- Analog Domain:
  - Inputs
  - SARADC1
  - SARADC2
  
- RTC Domain:
  - RTC ADC1 Controller
  - RTC ADC2 Controller
  
- Digital Domain:
  - Digital ADC1 Controller
  - Power / Peak Detect Controller

**Figure Caption:**
Figure 39.3-1. SAR ADC Overview

**Body Text under Figure (SAR ADC Overview):**

As shown in Figure 39.3-1, the SAR ADCs are managed by four dedicated controllers:
- One digital controller: digital ADC1 controller (DIG ADC1 controller), designed for high-performance multi-channel scanning and DMA continuous conversion.

**Footer Information:** 
Espressif Systems
Page number: 1465
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback