**Title: Chapter 39 On-Chip Sensors and Analog Signal Processing**

---

**Figure Caption:**  
Figure 39.2-6. Sensing Area

---

**Body Text:**
When operating in proximity mode, a touch sensor will take a fixed number of samples and accumulate those sampled values. If the final accumulated value exceeds a configured threshold, this indicates the detection of a proximate object and an interrupt will be triggered. Note that due to the accumulation of samples, a touch sensor operating in proximity mode will not generate the same values mentioned in section 39.2.71 (i.e., touch_raw_data, touch_smooth_data, and benchmark).

To operate in proximity mode:
- Configure a touch sensor to operate in proximity mode by setting SENS_TOUCH_APPROACH_PAD0, SENS_TOUCH_APPROACH_PAD1, or SENS TOUCH APPROACH_PAD2.
- Set RTC_CNTL TOUCH APPROACH MEAS TIME to adjust the number of samples taken to generate the accumulated value. The touch sensor maintains an internal sample counter to track the number of samples taken.
- Set the threshold value via SENS TOUCH OUT THN.

When the sample counter reaches RTC_CNTL TOUCH APPROACH MEAS TIME:
- If the accumulated value is larger than the threshold value, an interrupt will be triggered.
  - The sample counter and the accumulated value are reset to 0. The touch sensor will begin accumulating samples again.

---

**Subtitle: Section Title:**  
39.2.10 Moisture Tolerance

---

**Body Text:**
The presence of water droplets can lead to the detection of false touches. The **Moisture tolerance** feature can mitigate the effect of water droplets.
If the sensor array becomes wet (i.e., the majority of the sensor array is covered by water), the touch pads will no longer be able to detect finger touches. The Water Rejection feature can detect if the sensor array is wet and shut down the sensor array.

---

**Subtitle: Section Title:**  
39.2.10.1 Moisture Tolerance

---

**Body Text:**
The presence of water droplets on the touch pads can cause adjacent touch pads to be electrically coupled (if the water droplets are large enough to physically bridge two more adjacent touch pads). Coupled touch pads will lead to the false detection of touches due to the capacitance caused by the coupling.

To configure moisture tolerance:

---

**Footer:**
Espressif Systems  
1464  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)