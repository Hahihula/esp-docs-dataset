**Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)**

---

**Section Title:** Pin Hold Feature  
**Subtitle:** Digital Pins (GPIO26 ~ GPIO48)  

Each GPIO pin (including the RTC pins) has an individual hold function controlled by an RTC register. When the pin is set to hold, the state is latched at that moment and will not change no matter how the internal signals change or how the IO MUX/GPIO configuration is modified. Users can use the hold function for the pins to retain the pin state through a core reset triggered by watchdog time-out or Deep-sleep events.

- **Description:** The Hold state of each digital pin is controlled by the result of OR operation of the pin's Hold enable signal and the global Hold enable signal.
  - `RTC_CNTL_DIG_PAD_HOLD_REG[n]`, controls the Hold signal of each pin of GPIO26 ~ GPIO48.
  - `RTC_CNTL_DG_PAD FORCE_HOLD`, controls the global Hold signal of all digital pins.

To use this feature, follow these steps below:

- To maintain the pin's input/output status in Deep-sleep, set `RTC_CNTL_DIG_PAD_HOLD_REG[n]` to hold the value of each digital pin, \( n = 5 \sim 27 \), corresponding to GPIO26 ~ GPIO48. Or clear `RTC_CNTL_DIG_PAD_HOLD_REG[n]` to disable the Hold function of the pin.
- Alternatively, set `RTC_CNTL_DG_PAD FORCE_HOLD` to hold the values of all digital pins, or set `RTC_CNTL_DIG_PAD FORCE_UNHOLD` to disable the hold function of all digital pins.

---

**Section Title:** Pin Pins (GPIO0 ~ GPIO21)  

The Hold state of each RTC pin is controlled by the result of OR operation of the pin's Hold enable signal and the global Hold enable signal.
- `RTC_CNTL_RTC_PAD_HOLD_REG[n]` (\( n = 0 \sim 21 \)), controls the Hold signal of each pin of GPIO0 ~ GPIO21.

- `RTC_CNTL_RTC_PAD FORCE_HOLD`, controls the global Hold signal of all RTC pins.

To use this feature, follow these steps below:

- To maintain the pin's input/output status in Deep-sleep, set `RTC_CNTL_RTC_PAD_HOLD_REG[n]` (\( n = 0 \sim 21 \), corresponding to GPIO0 ~ GPIO21). Or clear the bits above to disable the Hold function of the pin.
- Alternatively, set `RTC_CNTL_RTC_PAD FORCE_HOLD` to hold the values of all RTC pins, or clear `RTC_CNTL_RTC_PAD FORCE_HOLD` to disable the hold function of all RTC pins.

---

**Section Title:** Power Supply and Management of GPIO Pins

**Subsection 6.10.1: Power Supply of GPIO Pins**

For more information on the power supply for GPIO pins, please refer to Pin Definition in [ESP32-S3 Datasheet](#).

---

**Subsection 6.10.2: Power Supply Management**

Each ESP32-S3 pin is connected to one of the three different power domains.

---

**Footer:**  
Espressif Systems  
481  
[Submit Documentation Feedback](#)  

ESP32-S3 TRM (Version 1.7)