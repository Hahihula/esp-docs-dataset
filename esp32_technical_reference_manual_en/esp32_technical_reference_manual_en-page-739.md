Title: Chapter 31 On-Chip Sensors and Analog Signal Processing

---

**Figure 31.2-2. Touch Sensor Structure**

[Diagram of touch sensor structure with components labeled as Bias, Sensor 0 to Sensor 9, T0 (Touch Pad), etc.]

Comparing the difference between the output pulse counts during the same time interval, we can conclude whether the touch pad has been touched. **TIE_OPT** is used to establish the initial voltage level that starts the charge/discharge cycle.

---

**Figure 31.2-3. Touch Sensor Operating Flow**

[Diagram showing different states of a touch sensor operating flow with labels such as START, TIE_OPT = 0 or 1, etc.]

---

Subtitle: **31.2.5 Touch FSM**

The Touch FSM performs a measurement sequence described in section 31.2.4. Software can operate the Touch FSM through dedicated registers. The internal structure of a touch FSM is shown in Figure 31.2-4.

The functions of Touch FSM include:

- Receipt of a start signal, either from software or a timer
  - when **SENS_SAR_TOUCH_START FORCE =** 1, **SENS_SAR_TOUCH START EN** is used to initiate a single measurement.
  - when **SENS_SAR_TOUCH START FORCE =** 0, measurement is triggered periodically with a timer.

The Touch FSM can be active in sleep mode. The **SENS_SAR_TOUCH SLEEP CYCLES** register can be used to set the cycles. The sensor is operated by RTC_FAST_CLK, which normally runs at 8 MHz. More information on that can be found in chapter Reset and Clock.

---

Footer: Espressif Systems  
Page Number: 739  
Document Title: ESP32 TRM (Version 5.6)  
Feedback Link Text: Submit Documentation Feedback